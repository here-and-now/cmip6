# CMIP6

This repository contains time series of annual-mean globally-averaged variables from various CMIP6 experiments, together with analysis of climate sensitivities, forcing and feedbacks.

## Global-mean anomaly time series

Anomalies are calculated by subtracting the trend in piControl calculated over the time period parallel to the perturbation experiment, as in [Andrews et al. (2012)](https://agupubs.onlinelibrary.wiley.com/doi/10.1029/2012GL051607) and [Forster et al. (2013)](https://agupubs.onlinelibrary.wiley.com/doi/full/10.1002/jgrd.50174). The final column is the multimodel mean.

|filename|description|
|--|--|
|`delta_tas_abrupt-4xCO2_cmip6.csv` | anomalies in surface air temperature [*tas*] relative to piControl in the abrupt-4xCO2 experiment|
|`delta_net_abrupt-4xCO2_cmip6.csv` | anomalies in net top-of-atmosphere flux [*rsdt - rsut - rlut*], relative to piControl in the abrupt-4xCO2 experiment|
|`delta_tas_1pctCO2_cmip6.csv` | anomalies in surface air temperature [*tas*] relative to piControl in the 1pctCO2 experiment|
|`delta_variable_experimentid_cmip6.csv` | anomalies in *variable* relative to piControl in the *experimentid* experiment


## Analysis

`gregory_plot_cmip6.csv`

Linear regression of anomaly in net top-of-atmosphere flux vs. anomaly in surface air temperature over the first 150 years of the abrupt-4xCO2 experiment, following [Gregory et al. (2004)](https://agupubs.onlinelibrary.wiley.com/doi/10.1029/2003GL018747). `gregory_plot_cmip6.txt` contains the same information in a plain text file.

`gregory_plot_fast_cmip6.csv` and `gregory_plot_slow_cmip6.csv`

As for the standard Gregory plot but using years 1-20 (*fast*) and years 21-150 (*slow*) of the abrupt-4xCO2 experiment respectively, following [Andrews et al. (2015)](https://journals.ametsoc.org/doi/full/10.1175/JCLI-D-14-00545.1)

|parameter|description|units|
|--|--|--|
|*Model*|CMIP6 Source ID||
|*F4x*|4xCO2 forcing (intercept)|W m<sup>-2</sup>|
|*lambda*|climate feedback (slope)|W m<sup>-2 </sup>K<sup>-1</sup>|
|*ECS*|effective climate sensitivity|K|
|*FSW*, *FLW*|shortwave and longwave components of *F4x*|W m<sup>-2</sup>|
|*lambdaSW*, *lambdaLW*|shortwave and longwave components of *lambda*|W m<sup>-2 </sup>K<sup>-1</sup>|

`tcr_cmip6.csv`

The transient climate response (TCR), derived from the 1pctCO2 experiment.

|parameter|description|units|
|--|--|--|
|*TCR*|*tas* anomaly averaged over years 61-80|K|
|*T140*|*tas* anomaly averaged over years 131-150|K|
|*ratio*|T140 / TCR |unitless|


`ohue_cmip6.csv`

Linear regression of anomaly in net top-of-atmosphere flux vs. anomaly in surface air temperature in the 1pctCO2 experiment, following [Gegory and Mitchell (1997)](https://agupubs.onlinelibrary.wiley.com/doi/abs/10.1029/97GL01930). The slope of the regression line is the ocean heat uptake efficiency (OHUE, *kappa*).

|parameter|description|units|
|--|--|--|
|*kappa_01_70*|*OHUE* calculated over years 1-70|W m<sup>-2 </sup>K<sup>-1</sup>|
|*kappa_71_140*|*OHUE* calculated over years 71-140|W m<sup>-2 </sup>K<sup>-1</sup>|


`two_layer_cmip6.csv`

Fit to the two-layer model of the surface air temperature anomalies in the abrupt-4xCO2 experiment using the method described in [Geoffroy et al. (2013)](https://journals.ametsoc.org/doi/full/10.1175/JCLI-D-12-00195.1).


|parameter|description|units|
|--|--|--|
| *tau_f* | fast (mixed layer) timescale |years|
| *tau_s* | slow (deep ocean) timescale |years|
| *gamma* | transfer co-efficient |W m<sup>-2</sup> K<sup>-1</sup>|
| *C* | mixed-layer heat capacity | W m<sup>-2</sup> K<sup>-1</sup> yrs |
| *C_O* | deep-ocean heat capacity | W m<sup>-2</sup> K<sup>-1</sup> yrs |
| *a_f*|contribution to *delta_tas* from the fast mode |unitless|
| *a_s*|contribution to *delta_tas* from the slow mode, *1 - a_f* |unitless|


### Acknowledgement

I acknowledge the World Climate Research Programme, which, through its Working Group on Coupled Modelling, coordinated and promoted CMIP6. I thank the climate modeling groups for producing and making available their model output, the Earth System Grid Federation (ESGF) for archiving the data and providing access, and the multiple funding agencies who support CMIP6 and ESGF.

### License

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0
International License][cc-by-sa].

[![CC BY-SA 4.0][cc-by-sa-image]][cc-by-sa]

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-image]: https://licensebuttons.net/l/by-sa/4.0/88x31.png
[cc-by-sa-shield]: https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg

