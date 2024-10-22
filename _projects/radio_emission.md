---
layout: page
title: Cosmic-Ray Electrons and Radio Emission in Merging Galaxy Clusters
description: simulations of relativistic electrons interacting with the ICM
img: assets/img/minihalo2.png
importance: 2
category: research
related_publications: true
---

A number of galaxy clusters contain diffuse, steep-spectrum radio emission. The most obvious of these are large,
extended sources (R ~ 1 Mpc) that are often found in merging clusters, known as "radio halos". There is a second class
of these features, found in the cool cores of more relaxed galaxy clusters (R ~ 100-200 kpc), known as "radio
minihalos." To be observed at frequencies of 100s of MHz to 1 GHz, the radio emission must be produced by relativistic
electrons with energies $$\gamma \sim 10^3 - 10^4$$. Since the time for cosmic-ray electrons (CRe) to diffuse across the
cluster is much longer than their radiative loss time at these energies, the electrons must either be reaccelerated by
some process or continuously injected *in situ*.

<div id="figure1" class="row" width=700px >
    <div class="col-sm mt-2 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/minihalo1.png" title="observed image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-2 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/minihalo2.png" title="simulated image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
Figure 1: Left: X-ray image of RXJ1720.1+2638 with radio contours overlaid. Right: Mock X-ray image with 
    mock radio contours overlaid from our reacceleration simulation in {% cite 2013ApJ...762...78Z %}.
</div>

CRe with energies $$\gamma \sim 10^2$$ may build up in the cluster volume due to acceleration by AGN and shocks and
production via hadronic processes. These electrons may then be reaccelerated by MHD turbulence driven by cluster
mergers. Relativistic particle reacceleration provides a natural explanation for the steepening of the spectrum at high
(~1 GHz) frequencies seen in many halos and minihalos, due to the competition of reacceleration and radiative losses. In
a cool core cluster, interactions with subclusters produce sloshing of the gas, which is observed in the X-ray band as
spiral-shaped cold fronts. [Mazzotta & Giacintucci 2008](https://ui.adsabs.harvard.edu/abs/2008ApJ...675L...9M) discovered
a correlation between sloshing cold fronts and radio minihalo emission in two galaxy clusters, and other examples have
been found since.

<div id="figure2" class="row" width=700px >
    <div class="col-sm mt-2 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/accel.png" title="observed image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-2 mt-md-0">
        {% include video.liquid path="assets/video/particles_emission.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=true %}
    </div>
</div>
<div class="caption">
Figure 2: Left: electron spectra at different epochs in our reacceleration simulation from 
   {% cite 2013ApJ...762...78Z %}. The initial spectrum with few high-energy particles is transformed into a 
   power-law spectrum extending to high energies. Right: the evolution of radio emission at a frequency of 327 MHz in our reacceleration simulation.
</div>

In line with this evidence, in {% cite 2013ApJ...762...78Z %} we performed a MHD simulation of gas sloshing in a cool-core cluster and
included the The sloshing produces MHD turbulence with $$\delta{v}$$ ~ 200 km/s onlength scales of ~10 kpc, which we
showed is capable of accelerating relativistic CRe up to the energies required for producing a minihalo. The spatial
distribution of the radio surface brightness and its spectrum are consistent with observed minihalos. In particular, the
minihalo emission is bounded by the sloshing cold fronts, exhibiting very sharp drops across cold front surfaces ([Figure 1](#figure1)).
Secondly, the minihalo emission is steep-spectrum, due to the trade-off between reacceleration and radiative losses on
the CRe at high energies ([Figure 2, left](#figure2)). Also, the minihalo is produced on a very short timescale (< 1 Gyr) and decays
afterward ([Figure 2, right](#figure2)). This is in line with the fact that not all cool-core clusters possess minihalos.  

In a subsequent work {% cite 2015ApJ...801..146Z %}, we studied the interplay of sloshing and the injection of relativistic CRe via hadronic interactions as an alternative hypothesis for the existence of radio mini-halos. In this scenario, the confinement of the radio emission to the volume bounded by the cold fronts is explained by the amplification of the magnetic field below the cold fronts ([Keshet & Loeb 2010](https://ui.adsabs.harvard.edu/abs/2010ApJ...722..737K)). This rapid field amplification is also held in this view to be responsible for the steepening of the CRe and radio spectra seen in minihalo (and radio halo) sources ([Keshet 2010](https://ui.adsabs.harvard.edu/abs/2010arXiv1011.0729K/abstract)).

<div class="row">
    <div id="figure3" class="col-sm mt-2 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/compare_profiles.png" title="radio emission profiles" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            Figure 4: Comparison of radial profiles of radio emission (normalized) from our
            reacceleration and hadronic models with the profiles from the minihalo source
            RXJ1720.1+2638 (see Figure 3a above). The drops in radio emission at the cold front
            surfaces in both the observation and the reacceleration simulation are very sharp, but
            are much shallower in the hadronic simulation.
        </div>
    </div>
    <div id="figure4" class="col-sm mt-2 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/spidx_map.png" title="spectral index map" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            Figure 5: Spectral index map from our simulation with 327 MHz radio contours overlaid.
            Some spectral steepening occurs along the cold front surface (seen in red), but the
            spectral index is only \(\Delta\alpha\) ~ 0.15 greater than the steady-state value of
            \(\alpha\) ~ 1.15.
        </div>
    </div>
</div>

We employed a simplified model where the hadronically generated CRe spectrum was allowed to deviate from a steady-state model due to rapid magnetic field amplification. In our simulation, diffuse radio emission with the power and spatial extent typical of mini-halos was produced. However, this emission had very different properties than that produced in our previous simulations using CRe reacceleration. Firstly, the emission was more extended, exhibiting only shallow drops across cold front surfaces [(Figure 3)](#figure3). Secondly, we found that the spectral steepening produced by rapid magnetic field amplification was marginal, resulting in a steepening of the radio spectral index $$\Delta\alpha$$ < 0.2 [(Figure 4)](#figure4), which is inconsistent with a number of minihalos with steeper spectra.
