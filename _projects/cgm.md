---
layout: page
title: The Hot Circumgalactic Medium
description: predicting X-ray signatures of gas motions and feedback around galaxies
img: assets/img/cgm_mock.png
importance: 2
category: research
related_publications: true
---

### Overview

Every galaxy is surrounded by a vast reservoir of diffuse gas, the circumgalactic medium (CGM), which extends out to its
virial radius and beyond. In galaxies with mass comparable to the Milky Way and above, a substantial fraction of this
gas is hot enough (10<sup>6</sup>-10<sup>7</sup> K) to emit primarily in X-rays. This hot phase is shaped by the same
processes that regulate galaxy evolution more broadly: cosmological accretion, galactic rotation, and outflows driven by
stellar and active galactic nucleus (AGN) feedback. Because the hot CGM is faint and diffuse, and the Milky Way has its
own hot CGM which is much brighter, it is generally not possible to observe it with current X-ray observatories such as
*Chandra* and *XMM-Newton*, except in bright nearby systems and only in the inner regions. However, future missions with
X-ray integral field unit (IFU) microcalorimeter instruments provide the spectral resolution to observe the emission
lines from the hot CGM in external galaxies which are cosmologically redshifted away from the bright lines of the Milky
Way (see [Figure 1](#figure1). Cosmological hydrodynamical simulations play a central role in predicting what these 
observations should show and in identifying which signatures can actually distinguish between competing models of 
galactic feedback.

<div id="figure3" class="row">
    <div class="col-sm mt-2 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/cgm_lxm_example.png" title="Mock Lynx images and spectra of the CGM in a MW-like galaxy." class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 1: Simulated Lynx observations of the CGM of a Milky Way-mass galaxy at z = 0.01 from the <a href="https://ui.adsabs.harvard.edu/abs/2019MNRAS.490.3196P">TNG 50 simulation</a>. The microcalorimeter resolution enables separation of the redshifted O VIIf, O VIII, and Fe XVII lines of the external galaxy from the Milky Way (MW) foreground, enabling maps of different gas phases (top panels) to be made from the narrow bands from the extracted spectrum from the circular region (bottom panel), as shown. The fact that the MW foreground (blue line) largely obscures the CGM from the extragalactic source (red line) highlights the necessity of high spectral resolution for this science.
</div>

### Mapping the Line-of-Sight Velocity Field of the Hot CGM

Because the hot CGM is optically thin and diffuse, any given line of sight through it can pass through gas
participating in several distinct kinds of motion at once: rotation co-planar with the galactic disk, inflows
associated with cosmological accretion, and outflows driven by stellar and AGN feedback. Disentangling these
components from real spectra requires first understanding, in a controlled simulated setting, how each contributes to
the velocity field and how well microcalorimeter-class spectral resolution can separate them.

In {% cite 2024ApJ...967...49Z %}, my collaborators and I used the TNG50 cosmological simulation to characterize the
line-of-sight velocity structure of the hot, X-ray-emitting CGM around a sample of nearby, Milky Way-mass simulated
disk galaxies, and generated synthetic X-ray observations to assess what future instruments could recover from it. We
found that stellar- and AGN-driven outflows produce the fastest, most readily detectable motions (roughly 200-500
km/s), while rotational motion in the hot gas is slower (roughly 100-200 km/s) but still measurable, particularly in
galaxies viewed close to edge-on. Slow inflows near the galactic plane (roughly 50-100 km/s), by contrast, are
difficult to isolate in projection, since they tend to be blended with faster components along the same sight line,
though multi-component spectral fitting may still be able to recover them. We also found that the velocity structure
inferred from the data is sensitive to which emission line is used to trace it, since different ions and transitions
preferentially trace gas at different temperatures, an important consideration for planning and interpreting future 
microcalorimeter observations of the CGM.

### X-ray Signatures of Galactic Feedback Across Simulation Models

The kinematic study above used a single simulation and feedback model, raising the question of how much these
predictions depend on the specific implementation of stellar and AGN feedback used in a given simulation, an
important question since different cosmological codes make substantially different choices for the subgrid physics
governing feedback.

In {% cite 2025ApJ...993..125S %}, my collaborators and I extended this approach across seven different cosmological
hydrodynamical simulation suites, examining 28 Milky Way-mass disk galaxies at redshift zero and comparing their
predicted X-ray surface brightness morphology, velocity structure, temperature distributions, and emission-line
signatures. We found that the X-ray brightness morphology of the hot CGM varies significantly from one feedback model
to another, with some simulations producing prominent outflow-enhanced regions and bubble-like structures while
others show much more azimuthally uniform emission; simulations lacking cosmic ray physics, however, consistently
produced radial surface brightness profiles well described by a single power law (roughly r<sup>-3</sup> between 20
and 200 kpc), with feedback physics primarily adding scatter around this trend rather than changing its slope.
Velocity maps revealed bulk rotation of the CGM together with high-velocity biconical outflows, most prominent in
simulations with strong AGN feedback, which also tended to produce extended regions of enhanced temperature in their
large-scale outflows; simulations including cosmic ray physics instead predicted systematically cooler CGM gas, since
cosmic ray pressure support suppresses some of the compressive heating present in purely thermal-feedback models.
Finally, we found that different emission lines trace distinct phases of the gas: lower-energy lines such as O VII
preferentially trace the volume-filling, quiescent component of the CGM, while higher-energy lines such as Fe XVII
selectively highlight the high-velocity, feedback-driven outflows, underscoring the value of combining multiple lines
to build a complete picture of the CGM's thermal and dynamical state with future X-ray missions.
