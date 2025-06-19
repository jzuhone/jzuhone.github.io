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

Various diagnostics of the solar wind environment are used in Chandra operations. These include:

* "Soft" protons measured by the [ACE](https://www.swpc.noaa.gov/products/ace-real-time-solar-wind) satellite; the ACE "P3" channel is the one that records the radiation that can cause significant damage to ACIS
* "Hard" protons measured by the [GOES](https://www.swpc.noaa.gov/products/goes-proton-flux) satellites
* The HRC GOES Proxy, which is a linear combination of GOES proton channels
* The ACIS txings rate, which appears to be related to the hard protons measured by GOES 

For a number of solar storms, I have cataloged and plotted the behavior of these various diagnostics over time for further analysis; these plots are hosted at the [ACIS Storm Pages](https://cxc.cfa.harvard.edu/acis/storms/). An example of such plots for a particular storm is shown in [Figure 1](#figure1) below.

<div id="figure1" class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/rad_vs_time.png" title="various solar radiation diagnostics vs. time" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
Figure 1: Example of time-series plots of various radiation diagnostics during a solar storm. From top to bottom, the panels show the ACE P3 flux, the ACIS threshold crossings rate, and the HRC Proxy. The pink shaded region marks the time the instruments were safed; the purple shaded regions mark normal radiation zone passages for each orbit of Chandra around the earth.
</div>

### ACIS txings Proxy

As mentioned above, the ACIS txings rates are currently the only solar radiation monitor on the spacecraft, and sharp rises in these rates correlate well with rises in the GOES proton data.

Motivated by this, in collaboration with my colleagues [John Soltis](https://johnsoltis.github.io) (Johns Hopkins University) and [Michelle Ntampaka](https://www.stsci.edu/~mntampaka/) (Space Telescope Science Institute), we have developed an early version of a "txings proxy" to predict the value of the txings rates during solar storms from the GOES proton data which is continuously updated in real-time. Since we only make three ~1-hour contacts with Chandra per day, and do not have real-time knowledge of the txings rates outside of these times, such a predictive proxy would be useful for two reasons: first, we can use a spike in the predicted rates to prepare for the possibility that we will come up on the next contact with the spacecraft with the likelihood that it has safed itself, and second we can use it to help decide when rates are low enough that it is safe to return to science. The txings rates are also only recorded when ACIS is taking data, so the proxy can also serve as an indicator of where the rates would be in between ACIS observations.

To produce this model, we have trained a dense neural network with [PyTorch](https://pytorch.org) on GOES proton and txings proxy data from 2022-2025. We employ cross-validation on this data with 10 different folds which are then split into training, validation, and test data. The main measure of the model's success is how often it correctly predicts that the txings rate will exceed the limit required to trigger a spacecraft safing action. We found that our model has an ~89% true positive rate for exceeding the limit and a ~8% false positive rate, which is more than adequate accuracy for use in real-time operations.

### Storm-related memos I have written

Any time there is a significant solar storm that causes actions to be taken by the ACIS Ops team, a memo is written. The following are memos I have written concerning some of these events. 

* [March 2023 Storm](../../assets/pdf/MAR2023_memo.pdf)
* [November 2023 Storm](../../assets/pdf/NOV2023_memo.pdf)
* [March 2024 Storm](../../assets/pdf/MAR2024_memo.pdf)
* [October 2024 Storm](../../assets/pdf/OCT2024_memo.pdf)

