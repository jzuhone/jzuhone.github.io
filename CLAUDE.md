# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

@AGENTS.md

The import above (`AGENTS.md`, which itself defers to `.github/copilot-instructions.md` and `docs/BOUNDARIES.md`) is the canonical short entry point: ownership boundaries, the validated command set, and PR-routing rules. Keep `AGENTS.md` short and ecosystem-neutral — put Claude-specific or longer-form guidance here instead. Everything below is the cross-repo "big picture" that those files assume but don't spell out.

## What this repo is

`al-folio` v1.x is a **thin Jekyll starter**, not a theme. It owns only: starter wiring (`Gemfile`, `_config.yml`, `_data/featured_plugins.yml`), example content (`_pages`, `_posts`, `_projects`, `_news`, `_teachings`, `_books`, `_bibliography`), docs (`docs/`), cross-gem integration tests (`test/integration_*.sh`), and visual/parity tests (`test/visual/`). **All runtime, layouts, includes, Sass, tags, filters, and feature JS live in versioned gems**, published independently on RubyGems. `docs/BOUNDARIES.md` is the authoritative area→gem ownership table.

The biggest recurring mistake is editing runtime here. If a change is layout/include/tag/filter/feature-behavior, it belongs in the owning gem (see routing below), not in this repo.

## The plugin ecosystem

Use the `al-folio-gem-routing` skill before routing any layout/include/tag/filter/feature-behavior change — it covers the sibling-gem architecture and the wrapper→tag→gem delegation map. One rule that's easy to violate without reading it: **never remove the v1 config contract keys** (`al_folio.api_version`, `style_engine`, `tailwind.*`, `distill.*`) — both a build-time hook and `al-folio upgrade audit` treat their removal as a blocking violation.

## Dev loop, Docker, and CI gates

Use the `al-folio-dev-testing` skill for the local command set (beyond AGENTS.md's validated set), Docker serving quirks, and what the CI style-contract/visual-regression gates actually check before you push.
