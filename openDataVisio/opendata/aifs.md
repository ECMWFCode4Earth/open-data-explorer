# AIFS (Artificial Intelligence Forecasting System) Data
---

The ECMWF AIFS determenistic model generates single forecast runs at 00, 06, 12, and 18 UTC. All AIFS parameters are freely and openly available.

```{note}
The AIFS ensemble model output data are not yet open to the public.
```

The AIFS products are released as soon as the data are produced. The open data are produced at 0.25 degrees resolution in GRIB edition 2 format.

More information about the file-naming convention is available on the [IFS](./ifs.md) (Integrated Forecasting System) Data webpage.

| File-naming convention | Values |
| -------- | ---- |
| ROOT | URL of a site hosting the open data |
| yyyymmdd | reference date |
| HH | 00, 06, 12, or 18 |
| model | AIFS |
| resol | 0p25 |
| stream | oper |
| step | forecast time step |
| U | unit of the time step (h) |
| type | fc |
| format | grib2 or bufr |