# AIFS (Artificial Intelligence Forecasting System) Data
---

The ECMWF AIFS determenistic model generates single forecast runs at 00, 06, 12, and 18 UTC. All AIFS parameters are freely and openly available.

```{note}
The AIFS ensemble model output data are not yet open to the public.
```

## The AIFS datasets
The AIFS products are released as soon as the data are produced. The open data are produced at 0.25 degrees resolution in GRIB edition 2 format.

More information about the file-naming convention is available on the [IFS](./ifs.md) (Integrated Forecasting System) Data webpage.

:::{table} File-naming convention of the ECMWF AIFS model outputs.
:label: tableAIFS
:align: center

| File-naming convention | Values |
| -------- | ---- |
| ROOT | URL of a site hosting the open data |
| yyyymmdd | reference date |
| HH | reference time |
| model | AIFS |
| resol | 0p25 |
| stream [^1] | oper |
| step | forecast time step |
| U | unit of the time step (h) |
| type [^1] | fc |
| format | grib2 or bufr |
:::

## Index files
To find out more about index files, visit the [IFS](./ifs.md) (Integrated Forecasting System) Data website.
```
{"domain": "g", "date": "20250608", "time": "0000", "expver": "0001", "class": "ai", "type": "fc", "stream": "oper", "step": "0", "levtype": "sfc", "param": "100v", "_offset": 0, "_length": 1382370}
```

[^1]: Further information can be found in [Appendix](../appendix.md).