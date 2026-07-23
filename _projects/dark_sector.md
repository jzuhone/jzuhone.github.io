---
layout: page
title: Galaxy Clusters as Laboratories for the Dark Sector
description: probing the nature of dark matter and alternative theories
img: assets/img/dm_collision.png
importance: 4
category: research
related_publications: true
---

### Overview

The mass budget of clusters is dominated by dark matter, which outweighs the baryonic (gas and stellar) mass by a 
factor of roughly five to one. This makes clusters powerful laboratories for studying the "dark sector": not only 
the detailed physical properties of dark matter itself, but even the question of whether the phenomena attributed 
to dark matter require a new particle species at all, as opposed to a modification of gravity. My work in this 
area has approached the problem from three different angles: using the dynamics of colliding clusters to probe 
the collisionless nature of dark matter, using the internal structure of merging clusters to constrain dark matter
self-interactions, and using the detailed mass profiles of relaxed clusters to test an alternative, purely 
gravitational explanation for "dark matter" phenomenology.

### Dark Matter Dynamics in Cluster Mergers: The Puzzle of Cl 0024+17

Because dark matter is thought to be very nearly collisionless, while the hot intracluster gas is a weakly 
collisional fluid, high-speed collisions between clusters can separate the two components spatially, producing
offsets between the total mass distribution (traced by gravitational lensing) and the gas distribution (traced by
X-rays). The most famous example is the "Bullet Cluster," but an even stranger case is the galaxy cluster Cl 0024+17, 
for which a weak- and strong-lensing mass reconstruction performed by [Jee et al. (2007)]((https://ui.adsabs.harvard.edu/abs/2007ApJ...661..728J/abstract))
revealed an unusual ringlike substructure in the dark matter distribution. In that same work, they proposed that 
this ring was produced by a high-speed, nearly head-on collision between two clusters 1-2 Gyr in the past, with 
the ring forming from the radially expanding, "splashback" of dark matter particles following pericentric passage.

<div id="figure1" class="row">
    <div class="col-sm mt-2 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/dm_ring.jpg" title="dark matter ring in Cl 0024+17" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 1: The ringlike dark matter substructure reconstructed from weak- and strong-lensing observations of Cl 0024+17 by Jee et al. (2007).
</div>

In {% cite 2009ApJ...696..694Z %}, my collaborators and I tested this scenario directly with N-body simulations of
cluster collisions, exploring a range of impact parameters, mass ratios, and initial velocity distributions for the
dark matter particles. We found that such collisions do produce a "shoulder" feature in the post-collision dark
matter distribution, but not a true ring, even when the initial velocity distribution is highly tangentially
anisotropic (see [Figure 1](#figure1)). A ring-like feature could only be reproduced by assuming a purely circular (tangential) initial velocity
distribution for the dark matter particles, which is not realistic for halos built up through hierarchical structure
formation in a cosmological context. We were therefore unable to find a fully satisfactory explanation for the dark
matter ring in Cl 0024+17 using standard collisionless dynamics, leaving open the possibility that the true
explanation involves either more complex merger geometries, projection effects, or physics beyond the standard
collisionless dark matter picture. However, a more likely explanation is that the ring structure may be an artifact
of the lensing analysis of [Jee et al. (2007)](https://ui.adsabs.harvard.edu/abs/2007ApJ...661..728J/abstract), as
later lensing studies of the same system did not find it (see, e.g. [Umetsu et al. 2010](https://ui.adsabs.harvard.edu/abs/2010ApJ...714.1470U/abstract))

### Testing Self-Interacting Dark Matter with Sloshing Cold Fronts

A more direct way to probe non-standard dark matter physics is to ask whether dark matter can interact with itself
beyond gravity via short-range interactions. Such self-interacting dark matter (SIDM) models are motivated in part 
by persistent small-scale puzzles in galaxy and cluster cores. Clusters that have undergone minor mergers frequently 
display "sloshing" cold fronts (see my page on [cold fronts](/projects/cold_fronts) for more on this phenomenon), 
spiral-shaped discontinuities in the X-ray-emitting gas that form because the collisionless dark matter and 
collisional gas respond differently to the gravitational perturbation of an infalling subcluster.

<div id="figure2" class="row">
    <div class="col-sm mt-2 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/sloshing_sidm.png" title="sloshing in SIDM" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 2: The evolution of cold fronts in a sloshing cluster core, for different values of the DM self-interacting cross section.
</div>

In {% cite 2019ApJ...882..119Z %}, my collaborators and I used combined N-body/hydrodynamic simulations to ask how
this picture changes if the dark matter itself has a nonzero self-interaction cross section. In an isolated cluster,
increasing the cross section flattens the dark matter density profile into a core, which produces a modest adiabatic
expansion and cooling of the gas near the cluster center. In merging clusters, cold fronts still form via the same
basic mechanism as in the collisionless case, but the flattened central potential allows the sloshing gas to expand
to somewhat larger radii early in its evolution (see [Figure 2](#figure2)). More strikingly, as the infalling subcluster's dark matter halo
passes through the core, self-interactions strip away its dark matter mass, weakening its gravitational influence on
the core gas; the resulting sloshing motions are slower than in the collisionless case, which suppresses the growth
of Kelvin-Helmholtz instabilities and the associated turbulent mixing and entropy generation at the cold fronts. For
cross sections per unit mass above roughly 1 cm<sup>2</sup> g<sup>-1</sup>, the infalling subcluster's dark matter
halo does not survive as a self-bound structure beyond about two core passages. We also found that the offset between
the peaks of the X-ray surface brightness and the thermal Sunyaev-Zel'dovich signal during sloshing is sensitive to
the dark matter cross section, potentially providing an independent, non-merger-based observational handle on dark
matter self-interactions.

### Testing Emergent Gravity as an Alternative to Dark Matter

Rather than probing the properties of a dark matter particle, one can instead ask whether the phenomena attributed to
dark matter require new matter at all, or whether they can be explained by a modification of gravity itself. [Erik
Verlinde's "Emergent Gravity"](https://ui.adsabs.harvard.edu/abs/2017ScPP....2...16V/abstract) proposes that the
apparent excess gravity attributed to dark matter emerges from the thermodynamics of the entanglement entropy of the 
de Sitter background, without invoking a new particle species, and makes a specific, parameter-free prediction for 
the "apparent" dark matter distribution given the observed baryon distribution (and vice versa). This prediction can 
be tested most cleanly in relaxed, massive clusters, where accurate mass profiles can be reconstructed from a 
combination of optical, X-ray, and weak-lensing data.

In {% cite 2019ApJ...880..145Z %}, we carried out this test using a sample of massive, dynamically
relaxed clusters, combining weak-lensing total mass profiles, *Chandra* X-ray mass profiles of the hot intracluster
gas, and, as an improvement over earlier work in this area, the stellar mass contribution of the brightest cluster
galaxy in each system. We found that including the brightest cluster galaxy improves the agreement between the EG
predictions and the observations in the innermost regions of the clusters (r ≲ 10-30 kpc), where the stellar mass of
the central galaxy dominates. However, at intermediate radii (r ~ 100-200 kpc) the EG predictions for the mass
profiles and baryon fractions are discrepant with the observations by a factor of up to roughly 2-6, with the
agreement improving again near r<sub>500</sub>. We concluded that, at least in its current form, Emergent Gravity
does not reproduce the observed mass distributions of relaxed galaxy clusters as well as the standard cold dark
matter picture.
