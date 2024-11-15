---
layout: page
title: Cosmic-Ray Electrons and Radio Emission in Merging Galaxy Clusters
description: simulations of relativistic electrons interacting with the ICM
img: assets/img/minihalo2.png
importance: 2
category: research
related_publications: true
---

### Overview

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

### Reacceleration Models for Mini-Halos

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

### Hadronic Models for Mini-Halos

In a subsequent work {% cite 2015ApJ...801..146Z %}, we studied an alternative hypothesis for the origin of radio mini-halos: the interplay of sloshing and the injection of relativistic CRe via hadronic interactions, which arise from collisions between cosmic-ray protons (CRp) and thermal protons in the ICM that produce secondary CRe. In this scenario, the confinement of the radio emission to the volume bounded by the cold fronts is explained by the amplification of the magnetic field below the cold fronts ([Keshet & Loeb 2010](https://ui.adsabs.harvard.edu/abs/2010ApJ...722..737K)). This rapid field amplification is also held in this view to be responsible for the steepening of the CRe and radio spectra seen in minihalo (and radio halo) sources ([Keshet 2010](https://ui.adsabs.harvard.edu/abs/2010arXiv1011.0729K/abstract)).

<div class="row">
    <div id="figure3" class="col-sm mt-2 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/compare_profiles.png" title="radio emission profiles" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            Figure 3: Comparison of radial profiles of radio emission (normalized) from our
            reacceleration and hadronic models with the profiles from the minihalo source
            RXJ1720.1+2638 (see Figure 3a above). The drops in radio emission at the cold front
            surfaces in both the observation and the reacceleration simulation are very sharp, but
            are much shallower in the hadronic simulation.
        </div>
    </div>
    <div id="figure4" class="col-sm mt-2 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/spidx_map.png" title="spectral index map" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            Figure 4: Spectral index map from our simulation with 327 MHz radio contours overlaid.
            Some spectral steepening occurs along the cold front surface (seen in red), but the
            spectral index is only \(\Delta\alpha\) ~ 0.15 greater than the steady-state value of
            \(\alpha\) ~ 1.15.
        </div>
    </div>
</div>

We employed a simplified model where the hadronically generated CRe spectrum was allowed to deviate from a steady-state model due to rapid magnetic field amplification. In our simulation, diffuse radio emission with the power and spatial extent typical of mini-halos was produced. However, this emission had very different properties than that produced in our previous simulations using CRe reacceleration. Firstly, the emission was more extended, exhibiting only shallow drops across cold front surfaces [(Figure 3)](#figure3). Secondly, we found that the spectral steepening produced by rapid magnetic field amplification was marginal, resulting in a steepening of the radio spectral index $$\Delta\alpha$$ < 0.2 [(Figure 4)](#figure4), which is inconsistent with a number of minihalos with steeper spectra.

### Redistribution of Cosmic Rays from Active Galactic Nuclei

Regardless of the model for the production of radio mini-halos (whether reacceleration or hadronic), the origin of the CRe to be reaccelerated or the CRp to produce the secondaries must still be explained. The most natural explanation for the prevalence of relativistic particles in the ICM is that they are injected by AGN. In {% cite 2021ApJ...914...73Z %}, we placed a black hole particle with an AGN jet into one of our sloshing simulations, varying the jet axis for different simulations, to determine how sloshing redistributes the cosmic-ray material from the jet (in this work, modeled by a simple tracer field that is advected along with the thermal gas). We found that the bulk motions and the turbulence from sloshing efficiently redistribute the jet material throughout the cluster core. Also, some of this material rises to a significant height and is then stretched by the sloshing motions, producing linear features in the projected CR distribution with magnetic fields aligned along the feature. We also explored a scenario where a bubble was placed at a large distance and was then redistributed, with similar results. From these results, we hypothesized that such long and thin features could be an explanation for some radio relics, assuming a shock from a later merger passes over them. Examples of these simulations are shown in [(Figure 5)](#figure5).

<div id="figure5" class="row">
<h4>Jets along x-axis:</h4>
</div>
<div class="row">
    <div class="col">
        {% include video.liquid path="assets/video/R5_b500_jets_x.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=true %}
    </div>
</div>
<div class="row">
<h4>Jets along y-axis:</h4>
</div>
<div class="row">
    <div class="col">
        {% include video.liquid path="assets/video/R5_b500_jets_y.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=true %}
    </div>
</div>
<div class="row">
<h4>Jets along z-axis:</h4>
</div>
<div class="row">
    <div class="col">
        {% include video.liquid path="assets/video/R5_b500_jets_z.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=true %}
    </div>
</div>
<div class="caption">
Figure 5: The evolution of the AGN jet material in a sloshing cluster core, from {% cite 2021ApJ...914...73Z %}. The three rows of panels show simulations where the jet fires along the x, y, and z axes, respectively. The sloshing motions are predominantly in the x-y plane. Left panels show the gradient of the X-ray surface brightness, whereas the right panels show the projected fraction of jet material. The sloshing motions effectively redistribute the jet material and produce features that appear similar to radio minihalos and radio relics in projection.
</div>

We followed up with a similar set of simulations in {% cite 2021Galax...9...91Z %}, only this time improving the physical description of the cosmic rays. In this work, we treated the cosmic rays as a separate fluid with $$\Gamma$$ = 4/3, and explored the effects of Alfvén cooling and spatial diffusion. The result was that the density of cosmic rays in the radio relic-like features was decreased. More study is needed to determine the likelihood that radio relics can be formed in this way. More recently {% cite 2024arXiv240619681D %} expanded the parameter space of mergers producing sloshing motions and AGN jets over {% cite 2021ApJ...914...73Z %}, to determine if the same subcluster that redistributed the CRs in the first place by setting off the sloshing motions could also produce radio relics by running over the CRs on a second or third pass. We found that such a scenario is very unlikely; in most cases the shocks from the second core passage are too weak to efficiently reaccelerate the CRs, so a separate merger is most likely needed.

