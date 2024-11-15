---
layout: page
title: ACIS Storms Analysis
description: protecting ACIS from space weather
img: assets/img/ace_p_jun2024.png
importance: 2
category: chandra
related_publications: false
---

### Overview

The Advanced CCD Imaging Spectrometer (ACIS) camera on the *Chandra* spacecraft is sensitive to damage from protons in
the solar wind with kinetic energies of ~100 keV, which can be reflected by the *Chandra* mirrors onto the CCDs and
increase charge transfer inefficiency (CTI), degrading the spectral resolution of the CCDs. When solar storms occur, it
is sometimes necessary to safe ACIS (shutting it down and moving it out of the focal plane) to prevent this radiation
damage. 

Shutdowns can be manually executed if the *Chandra* project judges the radiation environment to be too dangerous. There
is also a mechanism for an autonomous shutdown. Earlier in the mission, Chandra used the Electron Proton Helium
INstrument (EPHIN) on board to detect significant radiation levels and trigger autonomous instrument safing. EPHIN became
inoperable in 2013; at this point the High Resolution Camera (HRC) anti-coincidence shield rates were used to detect
solar storms. Beginning in 2020, HRC operations became reduced due to difficulties running the instrument at high
temperatures, so the shield rate could no longer be used as an "always-on" radiation monitor. 

The current radiation monitor aboard Chandra is the ACIS threshold crossings rate, or "txings" rate. The ACIS flight
computer and software detects and recognizes X-ray events during the length of an observation. The computer examines
each CCD frame to find pixels with detections above a pre-determined threshold value. Not all such events are X-rays;
this is determined by further processing. However, the total txings rate is calculated and telemetered to the ground.
This value is sensitive both to X-rays and to particles; because of the latter it can be used as a radiation monitor to detect solar storms and trigger autonomous safing of the science instruments.

### ACIS Storm Pages

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/rad_vs_time.png" title="various solar radiation diagnostics vs. time" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
Figure 1: Example of time-series plots of various radiation diagnostics during a solar storm from the [ACIS Storm Pages](https://cxc.cfa.harvard.edu/acis/storms/). From top to bottom, the panels show the ACE P3 flux, the ACIS threshold crossings rate, and the HRC Proxy. The pink shaded region marks the time the instruments were safed; the purple shaded regions mark normal radiation zone passages for each orbit of Chandra around the earth.
</div>

### Storm-related memos I have written

Any time there is a significant solar storm that causes actions to be taken by the ACIS Ops team, a memo is written. The following are memos I have written concerning some of these events. 

* [March 2023 Storm](../../assets/pdf/MAR2023_memo.pdf)
* [November 2023 Storm](../../assets/pdf/NOV2023_memo.pdf)
* [March 2024 Storm](../../assets/pdf/MAR2024_memo.pdf)
* [October 2024 Storm](../../assets/pdf/OCT2024_memo.pdf)

