---
layout: page
title: Gas Motions in the Intracluster Medium
description: Predicting and Explaining Observations
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

