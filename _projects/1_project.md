---
layout: page
title: Cold Fronts in the Hot Plasma of Galaxy Clusters
description: constraining plasma physics and explaining observations
img: assets/img/virgo_temp.png
importance: 1
category: research
related_publications: true
---

The latest generation of X-ray telescopes, including *Chandra* and *XMM-Newton*, have revealed the existence of sharp
surface brightness discontinuities which betray the existence of sharp density jumps in the intracluster medium (ICM)
Spectral analysis demonstrates that these are also jumps in temperature, with the denser side of the front having a
lower temperature. These features have been dubbed "cold fronts"; for reviews see [Markevitch & Vikhlinin
2007](http://adsabs.harvard.edu/abs/2007PhR...443....1M) and {% cite 2016JPlPh..82c5301Z %}. Simulations indicate that cold fronts may form
from merging activity, whether by ram-pressure stripping or "ram-pressure slingshots" of cool, dense gas. Cold fronts
should be susceptible to heat conduction, which would elminate the sharp temperature gradient on a short timescale, and
fluid instabilities, such as Kelvin-Helmholtz (K-H), which would disrupt their smooth appearance.

However, many cold fronts are observed to be very smooth and sharp, so there must be a mechanism to support the existence of these features. One possible mechanism is magnetic fields. The velocity shear associated with a cold front can amplify the weak cluster magnetic fields to near-equipartition strengths, and stretch the field lines tangential to the front surface (Figure 1b). Due to the small Larmor radii of electrons in the $\mu$G cluster magnetic field, heat conduction is strongly anisotropic, occurring essentially only along the field lines. Therefore, a magnetic field stretched parallel to the front surface would shield the temperature gradient from heat conduction. In {% cite 2011ApJ...743...16Z %} we performed a series of simulations of sloshing cold front formation in a magnetized ICM. We varied the overall magnetic field strength of the cluster and the degree to which it is tangled on small scales. We found that for initial magnetic field energies ~1% of the thermal energy, the field is stretched and amplified to such a degree that most cold fronts can be stabilized against the development of fluid instabilities (Figure 2). Large-radii cold fronts, where the field is weaker, are more susceptible to the development of instabilities.

<div class="row">
    <div class="col-sm mt-2 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/temps.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-2 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/bfields.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="row">
    <div class="col-sm mt-2 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/virgo_temp.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-2 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/virgo_counts.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>

You can also put regular text between your rows of images, even citations {% cite einstein1950meaning %}.
Say you wanted to write a bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, _bled_ for your project, and then... you reveal its glory in the next row of images.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>

The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

{% raw %}

```html
<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-4 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
```

{% endraw %}
