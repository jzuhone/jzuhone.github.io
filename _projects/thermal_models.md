---
layout: page
title: Chandra/ACIS Thermal Modeling
description: Keeping ACIS within its limits
img: assets/img/thermal_model_example.png
importance: 1
category: operations
related_publications: false
---


My main role on the ACIS Operations team is to develop software for thermal modeling of various components on the ACIS instrument. Various factors, including sunlight, electronic components, and passive cooling into space affect ACIS temperatures. To prevent components on _Chandra_ from getting too hot (or sometimes too cold), the CXC has developed the Python-based [xija](https://github.com/sot/xija) thermal modeling framework to solve physically motivated ODEs with model coefficients fitted to historical temperature data. I have participated in the development of this package, as well as driven the development of an ACIS-specific package, [acis_thermal_check](https://github.com/acisops/acis_thermal_check), to run thermal model predictions for Chandra schedules and validate the results against historical data. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/thermal_model_example.png" title="ACIS Focal Plane thermal model example" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
