# IFS (Integrated Forecasting System) Data
---

In our tutorials we will use the subset of free and open IFS parameters. The open data are a product of the high-resolution and ensemble as well as seasonal forecast models.

```{dropdown} Medium-range and long-range forecast models 
The medium-range forecasts consist of a high-resolution (HRES) forecast and the ensemble (ENS) which provide the information about the evolution of weather up to 15 days ahead. HRES is a single forecast which describes one possible evolution of the weather out to 10 days ahead. ENS is a probabilistic forecast system of 51 forecasts. One is a control forecast, the other 50 forecasts are produced with slightly altered initial conditions and model physics. ENS indicates the range of possible weather conditions out to 15 days ahead, including the probability of occurrence of particular weather events.

The long-range (seasonal) forecast provide information about the Earth system components (atmosphere, ocean, land) up to 7 months into the future.
```

These products are produced at 0.25 degrees resolution in GRIB edition 2 format and are available 1 hour after the real-time dissemination schedule. The files are named as `ROOT`/`yyyymmdd`/`HH`z/`model`/`resol`/`stream`/`yyyymmdd` `HH`0000-`step` `U`-`stream`-`type`.`format`.

| File-naming convention | Values |
| -------- | ---- |
| ROOT | URL of a site hosting the open data |
| yyyymmdd | reference date |
| HH | 00, 06, 12, or 18 |
| model | IFS |
| resol | 0p25 |
| stream | oper, enfo, waef, wave, scda, scwv, or mmsf |
| step | forecast time step |
| U | unit of the time step (h or m; m only for mmsf) |
| type | fc, ef, ep, or tf |
| format | grib2 or bufr |

The valid combinations are in detail described [here](https://confluence.ecmwf.int/display/DAC/ECMWF+open+data%3A+real-time+forecasts+from+IFS+and+AIFS).