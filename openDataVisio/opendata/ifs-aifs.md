# IFS and AIFS
---

ECMWF open data policy includes data from both the Integrated Forecasting System ([IFS](https://www.ecmwf.int/en/forecasts/datasets/open-data)) and the Artificial Intelligence Forecasting System ([AIFS](https://www.ecmwf.int/en/forecasts/datasets/set-ix)) models. The data is provided at the highest available resolution. They are released under a Creative Commons Attribution 4.0 International licence, allowing for commercial and non-commercial use with appropriate attribution. <br>

Open data are a product of the high-resolution and ensemble as well as seasonal forecast models.

```{attention}
The seasonal forecast model output data are not yet open to the public.
```

```{dropdown} Medium-range and long-range forecast models 
The medium-range forecasts consist of a high-resolution (HRES) forecast and the ensemble (ENS) which provide the information about the evolution of weather up to 15 days ahead. HRES is a single forecast which describes one possible evolution of the weather out to 10 days ahead. ENS is a probabilistic forecast system of 51 forecasts. One is a control forecast, the other 50 forecasts are produced with slightly altered initial conditions and model physics. ENS indicates the range of possible weather conditions out to 15 days ahead, including the probability of occurrence of particular weather events.

The long-range (seasonal) forecast provide information about the Earth system components (atmosphere, ocean, land) up to 7 months into the future.
```

## IFS (Integrated Forecasting System) Data

In our tutorials we will use the subset of free and open IFS parameters which are available since 12 November 2024. The IFS model generate forecasts runs at 00, 06, 12, and 18 UTC.

:::{seealso}
Further information about the IFS model can be found [here](https://confluence.ecmwf.int/display/FCST/Implementation+of+IFS+Cycle+49r1).
:::

## AIFS (Artificial Intelligence Forecasting System) Data

The ECMWF AIFS determenistic model is a machine learing-driven model that generates single forecast runs at 00, 06, 12, and 18 UTC. It uses the operational IFS control initial condition. All AIFS parameters are freely and openly available. The current verion of the AIFS-Single has been operating since 25 February 2025.

:::{seealso}
Further information about the AIFS Single model can be found [here](https://confluence.ecmwf.int/display/FCST/Implementation+of+AIFS+Single+v1).
:::

```{note}
In two case studies, we analysed open AIFS parameters which were retieved from `aifs` and not `aifs-single` forecasts datasets. These data are made accessible to users before February 2025. 
```

## AIFS Ensemble Data

A first version of the probabilistic model of the AIFS has been operational since 1 July 2025. The ECMWF AIFS ensemble model uses machine learning to generate ensemble forecasts runs at 00, 06, 12, and 18 UTC. The AIFS ENS produces multiple forecast scenarios which represent uncertainty in weather predictions. By introducing different random perturbations of the initial conditions of an IFS ENS member, AIFS ENS is comprised of 50 perturbed members and a control member which is initialised from the unperturbed initial conditions of the IFS ENS control member. The control member of the AIFS ENS includes model perturbations in its forecast in contrast to the IFS ENS. In medium-range forecasts, it outperforms the ECMWF’s traditional physics-based ensemble system according to the recent verification statistics and evaluations.

:::{seealso}
Further information about the AIFS Ensemble model can be found [here](https://confluence.ecmwf.int/display/FCST/Implementation+of+AIFS+ENS+v1).
:::

Currently, a subset of the products provided by AIFS are also available in AIFS ENS.