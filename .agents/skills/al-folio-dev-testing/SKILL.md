---
name: al-folio-dev-testing
description: Use when running the local dev server, tests, or Docker for this al-folio v1.x site, or when checking what CI enforces before pushing — covers the daily dev command loop, Docker serving quirks, and the CI gates/style contract.
---

# al-folio Dev Loop, Docker, and CI Gates

## Daily dev loop

```bash
bundle install                                # ruby gems
bundle exec jekyll serve                      # dev server → http://localhost:4000/al-folio/  (NOTE baseurl)
bundle exec jekyll build --baseurl /al-folio  # production-style build to _site/
bash test/integration_distill.sh             # run ONE integration test (any of the five)
npm run test:visual:update                    # refresh playwright snapshots after intentional UI change
bundle exec al-folio upgrade apply --safe     # deterministic codemods (font-weight-* → font-*, remote→local URLs)
bundle exec al-folio upgrade overrides diff <path>    # then `overrides accept <path>` to acknowledge an override
```

`bin/setup-python-deps` installs the optional Python toolchain in `requirements.txt` (`nbconvert` for `jekyll-jupyter-notebook`, `rendercv[full]` for CV rendering, `scholarly` for `bin/update_scholar_citations.py`). Responsive-image generation (`imagemagick.enabled: true`) needs ImageMagick `convert` on PATH. `bin/deploy` is the manual `gh-pages` build+purgecss+force-push path (CI normally deploys).

## Docker serving model (v1-specific)

`docker compose up -d` bind-mounts the repo to `/srv/jekyll` and runs `bin/entry_point.sh`, which serves with `--force_polling --destination /tmp/_site`. The build output deliberately goes to **container-local `/tmp/_site`, not the bind-mounted `_site`** — writing `_site` back across the host bind mount caused write deadlocks. The container also `inotifywait`s `_config.yml` and restarts Jekyll on change (config edits aren't hot-reloaded by `--watch`). Verify with the `/al-folio` baseurl: `curl -fsS http://127.0.0.1:8080/al-folio/`. `docker-compose-slim.yml` pulls a prebuilt `:slim` image instead of building locally.

Note: this site's own `_config.yml` has a blank `baseurl`, so its Docker/dev server is actually reachable at `http://127.0.0.1:8080/` (root), not `/al-folio/` — the `/al-folio/` path above is the generic v1 starter convention and doesn't apply here.

## CI gates and the style contract

`npm run lint:style-contract` (`test/style_contract.js`) is the automated enforcement of the thin-starter boundary, and it will fail CI if you cross it: the starter must **not** define `build:css`/`build:tailwind` npm scripts, must **not** own `_includes`/`_layouts`/`_sass`/`_scripts`/`assets/tailwind`/`tailwind.config.js`/icon-font artifacts, must keep `theme: al_folio_core` and the required plugins in `_config.yml`, and must keep the `third_party_libraries` SRI pins and `al_math` Gemfile pin. Other gates: `unit-tests.yml` (style contract + the five integration scripts), `visual-regression.yml` (Playwright chromium+webkit, diffs candidate against a v0.16.3 baseline served on :4100 via `BASELINE_URL`), `upgrade-check.yml` (`al-folio upgrade audit`), `prettier.yml`. Prettier uses `@shopify/prettier-plugin-liquid` with `printWidth: 150`; run `npm run lint:prettier` before pushing.
