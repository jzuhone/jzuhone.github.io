---
layout: page
title: Cold Fronts in the Hot Plasma of Galaxy Clusters
description: constraining plasma physics and explaining observations
img: assets/img/virgo_temp.png
importance: 1
category: research
related_publications: true
---

### Overview

The latest generation of X-ray telescopes, including *Chandra* and *XMM-Newton*, have revealed the existence of sharp
surface brightness discontinuities which betray the existence of sharp density jumps in the intracluster medium (ICM)
Spectral analysis demonstrates that these are also jumps in temperature, with the denser side of the front having a
lower temperature. These features have been dubbed "cold fronts"; for reviews see [Markevitch & Vikhlinin
2007](http://adsabs.harvard.edu/abs/2007PhR...443....1M) and {% cite 2016JPlPh..82c5301Z %}. Simulations indicate that cold fronts may form
from merging activity, whether by ram-pressure stripping or "ram-pressure slingshots" of cool, dense gas. Cold fronts
should be susceptible to heat conduction, which would elminate the sharp temperature gradient on a short timescale, and
fluid instabilities, such as Kelvin-Helmholtz (K-H), which would disrupt their smooth appearance.

### The Effects of Magnetic Fields on Cold Fronts

However, many cold fronts are observed to be very smooth and sharp, so there must be a mechanism to support the
existence of these features. One possible mechanism is magnetic fields. The velocity shear associated with a cold front
can amplify the weak cluster magnetic fields to near-equipartition strengths, and stretch the field lines tangential to
the front surface ([Figure 1](#figure1), left). Due to the small Larmor radii of electrons in the $$\mu$$G cluster
magnetic field, heat conduction is strongly anisotropic, occurring essentially only along the field lines. Therefore, a
magnetic field stretched parallel to the front surface would shield the temperature gradient from heat conduction. In {%
cite 2011ApJ...743...16Z %} we performed a series of simulations of sloshing cold front formation in a magnetized ICM.
We varied the overall magnetic field strength of the cluster and the degree to which it is tangled on small scales. We
found that for initial magnetic field energies ~1% of the thermal energy, the field is stretched and amplified to such a
degree that most cold fronts can be stabilized against the development of fluid instabilities ([Figure 1](#figure1),
right). Large-radii cold fronts, where the field is weaker, are more susceptible to the development of instabilities.

<div id="figure1" class="row">
    <div class="col-sm mt-2 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/bfields.png" title="magnetic fields" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-2 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/temps.png" title="temperatures" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 1: Slices through \(\beta\) (ratio of the thermal to magnetic pressures, left) and gas temperature (right) for a suite of simulations with varying initial magnetic field strength, from {% cite 2011ApJ...743...16Z %}. As the initial magnetic field strength is increased, Kelvin-Helmholtz instabilities are increasingly suppressed.
</div>

However, we found that the ability of magnetic fields to suppress heat conduction across cold fronts in this scenario is limited. In {% cite 2013ApJ...762...69Z %} we re-simulated our magnetized sloshing cold fronts with anisotropic thermal conduction. We found that despite the formation of magnetic field lines draped tangentially to the front surfaces, conduction is not fully suppressed and the temperature jumps can be significantly reduced, to the point where the corresponding surface brightness jumps would not be seen in observations. This is due to the fact that the magnetic field layers are not perfectly aligned with the cold front surfaces, and some heat flux is able to "leak through." This potentially places strong constraints on heat conduction in the bulk of the ICM.

Another candidate for preventing the development of fluid instabilities at cold front surfaces is viscosity. Little is currently known about the Reynolds number of the cluster plasma. Even a modest isotropic ion viscosity is capable of preventing the development of K-H instabilities at sloshing cold fronts, as was shown to a certain extent by {% cite 2010ApJ...717..908Z %} and in fuller depth by [Roediger et al. 2013](https://ui.adsabs.harvard.edu/abs/2013ApJ...764...60R/abstract).

However, for similar reasons as conduction, the ion viscosity in the ICM should be highly anisotropic. Therefore, the suppression of instabilities will be weaker and dependent upon the magnetic field direction. In {% cite 2015ApJ...798...90Z %} we performed a set of simulations of gas sloshing with magnetic fields and various models for viscosity. We found that the combination of even weak magnetic fields and Braginskii (anisotropic) viscosity is sufficient to produce cold fronts that are consistent with observations in terms of supressing K-H instabilties. We also found that this situation may be approximated by an isotropic Spitzer viscosity with a suppression factor of f ~ 0.1 ([Figure 2](#figure2)). However, we also showed that the effect of the magnetic field is crucial; even if the viscosity is the same, simulations with and without magnetic fields produce qualitatively different results in terms of the degree of disruption of cold front surfaces by instabilities.

<div id="figure2" class="row">
    <div class="col-sm mt-2 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/virgo_temp.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-2 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/virgo_counts.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 2: Temperature slices (left) and projected X-ray counts images (right) for simulations with different models for viscosity, from {% cite 2015ApJ...798...90Z %}. The "Inviscid" results in prevalent K-H instabilities along most of the fronts, whereas the simulations with viscosity suppress these instabilities to varying degrees.
</div>
