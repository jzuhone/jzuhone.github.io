---
layout: page
title: Gas Motions in the Intracluster Medium
description: predicting and explaining Observations
img: assets/img/big_cross.png
importance: 3
category: research
related_publications: true
---

Direct measurements of ICM velocities are limited. The *Hitomi* X-ray Observatory was launched in 2016 and made the
first direct ICM measurements of Doppler shifting and broadening of emission lines in the Perseus Cluster, using its
microcalorimeter instrument ([Hitomi Collaboration et al.
(2016)](https://ui.adsabs.harvard.edu/abs/2016Natur.535..117H/abstract), [Hitomi Collaboration et al.
(2018)](https://ui.adsabs.harvard.edu/abs/2018PASJ...70....9H/abstract)), and the follow-up *XRISM* mission has recently
observed a number of galaxy clusters. I am currently a Guest Scientist with the XRISM team, involved primarily on the
Perseus and Coma target teams. 

The Coma Cluster is a bright and nearby system which shows signs of recent merging. It has a large (~300 kpc) nearly constant-density core region, implying that the gas has little stratification. There is no central active galactic nucleus as there is in other clusters (like Perseus). Coma is therefore an ideal system to study the properties of ICM turbulence.

In {% cite 2016ApJ...817..110Z %}, I presented a strategy for mapping the turbulent velocity field in the Coma Cluster with Hitomi. Velocity turbulence can be characterized by a power spectrum, which is a function P(k) giving the amount of power in the velocity field at a given inverse length scale (or wavenumber) k. The power spectrum can constrain important physical properties like the injection scale of motions, the viscous dissipation scale, and the slope of the turbulent cascade in between these scales. Since this quantity is determined in Fourier space, it is difficult to measure in real observations, which are often not spatially continuous. Instead, the second-order velocity structure function can be calculated, which is the average squared difference between pairs of velocities for a given spatial separation, or:

$$SF(\ell) = \langle{[{\bf v}({\bf r} + {\bf \ell})-{\bf v}({\bf r})]^2}\rangle$$

This quantity (up to constant additive and mulplicative factors) is directly related to the power spectrum via the Fourier transform, and it can be calculated for any arbitrary set of points on the sky on which the velocity is measured. In {% cite 2016ApJ...817..110Z %}, we showed that while *Hitomi* would not be able to constrain the viscous dissipation scale due to its limited angular resolution, by spreading out the velocity measurements over a wide angular scale the injection scale of turbulence 
could be recovered ([Figure 1](#figure1)). These insights are currently being used in the analysis and interpreation of the recently obtained *XRISM* observations of the Coma Cluster. 

<div id="figure1" class="row">
    <div class="col-sm mt-2 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/big_cross.png" title="coma pointing strategy" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-2 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/sf.png" title="measured structure function" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 1: Left: a mock projected velocity map from {% cite 2016ApJ...817..110Z %}, binned to ~1.5 arcminute regions, the approximate angular resolution obtainable with Hitomi for the Coma velocity field. Red squares show the locations of suggested pointings for the *Hitomi* microcalorimeter detector. Right: computed velocity structure function from these pointings, including the effects of statistical and systematic measurement errors. 
</div>

Cool-core galaxy clusters (such as Perseus, Abell 2029, Centaurus, etc.) are also the sources of interesting gas motions, despite being more relaxed. These are turbulence driven by central active galactic nuclei (AGN), and the "sloshing" gas motions driven by mergers and associated with cold fronts (see the page on [cold fronts](/projects/cold_fronts) for more details). In this case, the cooler, denser gas below the front surface is moving at roughly 30-50% of the local sound speed, which should be detectable with microcalorimeter instruments such as *Hitomi* and *XRISM* if some of those motions are directed along the sight line. 

In {% cite 2016ApJ...821....6Z %} we made predictions for what Doppler shifting and broadening signatures such sloshing motions would make using mock *Hitomi* (then called *Astro-H*) observations of FLASH hydrodynamic simulations of core gas sloshing (notably without AGN feedback included). We explored two simulations, one inviscid, and another with Spitzer viscosity. The latter is unrealistic in the ICM due to the effect of magnetic fields making viscosity anisotropic, but serves as a useful extreme test for the effect of viscosity on line shapes due to velocities.

We found that in the case of sloshing, the line broadening is not changed significantly in the presence of such extreme viscosity (at least on the spatial scales at which *Hitomi* was able to observe given its ~1-arcminute PSF). This is because the origin of the majority of the line broadening is from the bulk sloshing motions themselves and not turbulent motions at smaller scales, which are more effectively damped by viscosity. A mission with higher angular resolution would be capable of measuring velocity differences across the cluster core and thereby constrain them on smaller scales to more effectively probe viscosity. 

<div id="figure2" class="row">
    <div class="col-sm mt-2 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/novisc_map_kT.png" title="temperature slice, no viscosity" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-2 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/visc_map_kT.png" title="temperature slice, with viscosity" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="row">
    <div class="col-sm mt-2 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/novisc_lines.png" title="line broadening, inviscid" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="row">
    <div class="col-sm mt-2 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/visc_lines.png" title="line broadening, viscous" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 2: Velocity fields in simulations with different viscosities are different, but produce similar line shapes. Top panels: Slices through gas temperature are shown for a inviscid (left) and viscous (right) simulation, where the lines indicate the regions (x1 and x2) used to extract a spectrum (in this case the observer's line of sight is in the plane of the image/screen). Middle panel: "toy" Fe-Kα lines, unshifted and unbroadened by velocities (blue) and shifted and broadened (green). In both regions x1 and x2, there is noticeable shifting and broadening. Bottom panel: The same lines for the viscous case, where they look very similar to the inviscid case. 
</div>

Thus, when Perseus was later observed by *Hitomi* ([Hitomi Collaboration et al.
(2016)](https://ui.adsabs.harvard.edu/abs/2016Natur.535..117H/abstract), [Hitomi Collaboration et al.
(2018)](https://ui.adsabs.harvard.edu/abs/2018PASJ...70....9H/abstract)), and it was reported that the gas motions in the core were quiescent, this does not necessarily imply that viscosity is strong, as shown in {% cite 2016ApJ...821....6Z %}, it simply means that the drivers of motions are not strong. It is also the case that for the stratified atmospheres of cool-core clusters, projection effects dictate that the length scales at which velocities are being measured strongly depend on the distance from the cluster core (see [Zhuravleva et al. 2012](https://ui.adsabs.harvard.edu/abs/2012MNRAS.422.2712Z/abstract)), such that dispersions in the center must necessarily be measured to be smaller. We explored these effects in more detail after publication of the *Hitomi* measurements in {% cite 2018ApJ...853..180Z %}, showing the effects of varying the line of sight with respect to the sloshing motions and the gradients of velocity across the cluster core that are produced in both inviscid and viscous cases ([Figure 3](#figure3)).

<div id="figure3" class="row">
    <div class="col-sm mt-2 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/compare_mu_novisc.png" title="mock velocity observations, no viscosity" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-2 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/compare_mu_visc.png" title="mock velocity observations, with viscosity" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 3: Mock Hitomi observations of gas velocities in a sloshing cluster core from {% cite 2018ApJ...853..180Z %}. The mock observations (bottom) showed that Hitomi was unable to strongly distinguish between inviscid and viscous models for the ICM (shown in idealized maps, top), and that therefore the core of Perseus is likely inherently quiescent.
</div>
