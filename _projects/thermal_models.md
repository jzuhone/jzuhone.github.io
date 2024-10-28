---
layout: page
title: Chandra/ACIS Thermal Modeling
description: Keeping ACIS within its limits
img: assets/img/thermal_model_example.png
importance: 1
category: chandra
related_publications: false
---

### Overview

My main role on the ACIS Operations team is to develop software for thermal modeling of various components on the ACIS instrument. Various factors, including sunlight, electronic components, and passive cooling into space affect ACIS temperatures. To prevent components on _Chandra_ from getting too hot (or sometimes too cold), the CXC has developed the Python-based [xija](https://sot.github.io/xija) thermal modeling framework to solve physically motivated ODEs with model coefficients fitted to historical temperature data. I have participated in the development of this package, as well as driven the development of three other packages to aid in _Chandra_ thermal modeling. 

The first is an ACIS-specific package, [acis_thermal_check](https://cxc.cfa.harvard.edu/acis/acis_thermal_check), that run thermal model predictions for _Chandra_ schedules for ACIS-specific temperatures and validates the results against historical data. We run these predictions on a weekly basis (and sometimes more often, depending on what is happening with the spacecraft), and the runs are archived and displayed [here](https://cxc.cfa.harvard.edu/acis/Thermal/).

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/thermal_model_example.png" title="ACIS Focal Plane thermal model example" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    A sample thermal model run of the ACIS Focal Plane temperature. The blue curve is the temperature prediction, and the magenta curve is the spacecraft pitch angle. The horizontal broken line with different colors indicates the thermal limit at any given moment, which depends on the type of observation being carried out. Bracketed line segments with numbers indicate the different observations and their IDs. Dashed vertical lines indicate periods of Chandra's entry into Earth's radiation belts, when it is not observing.
</div>

The second package I have played a central role in developing is [chandra_limits](https://cxc.cfa.harvard.edu/acis/chandra_limits), which is the package that determines which thermal limits should be adhered to as a function of time, depending on spacecraft states and observational characteristics. 

The third package I have developed is [ACISpy](https://cxc.cfa.harvard.edu/acis/acispy), which is designed to unify the analysis and visualization of _Chandra_ engineering telemetry archive and commanded states data and thermal model outputs into a single, unified framework. 

### Other pages related to ACIS thermal modeling and analysis

* [Current ACIS Load Real-Time](https://cxc.cfa.harvard.edu/acis/current_load_page/): A real-time page showing the current place in the observing schedule and current thermal models compared to real-time thermal-related telemetry.
* [ACIS FP Temperature and 1CRAT at Every Perigee](https://cxc.cfa.harvard.edu/acis/cr_fp_plots/index.html): We track the ACIS Focal Plane and Cold Radiator temperatures at every perigee, since they typically reach their maxima for a given week at these times, for health and safety reasons. 

### Thermal-related Memos I have written

* [Deciphering the Causes of the Anomalous Increase in Belt ECS Cold Time Between Epochs 85 and 86](../../assets/pdf/cold_time_anomaly.pdf)
* [Raising the 1DEAMZT Planning, Yellow, and Red Limits](../../assets/pdf/dea_limit.pdf)