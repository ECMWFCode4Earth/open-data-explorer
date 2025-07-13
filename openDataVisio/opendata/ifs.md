# IFS (Integrated Forecasting System) Data
---

In our tutorials we will use the subset of free and open IFS parameters. The open data are a product of the high-resolution and ensemble as well as seasonal forecast models.

```{dropdown} Medium-range and long-range forecast models 
The medium-range forecasts consist of a high-resolution (HRES) forecast and the ensemble (ENS) which provide the information about the evolution of weather up to 15 days ahead. HRES is a single forecast which describes one possible evolution of the weather out to 10 days ahead. ENS is a probabilistic forecast system of 51 forecasts. One is a control forecast, the other 50 forecasts are produced with slightly altered initial conditions and model physics. ENS indicates the range of possible weather conditions out to 15 days ahead, including the probability of occurrence of particular weather events.

The long-range (seasonal) forecast provide information about the Earth system components (atmosphere, ocean, land) up to 7 months into the future.
```

## The IFS datasets
These products are produced at 0.25 degrees resolution in GRIB edition 2 format and are available 1 hour after the [real-time dissemination schedule](https://confluence.ecmwf.int/display/DAC/Dissemination+schedule). The files are named as `ROOT`/`yyyymmdd`/`HH`z/`model`/`resol`/`stream`/`yyyymmdd` `HH`0000-`step` `U`-`stream`-`type`.`format`.

:::{table} File-naming convention of the ECMWF IFS model outputs.
:label: tableIFS
:align: center

| File-naming convention | Values |
| -------- | ---- |
| ROOT | URL of a site hosting the open data |
| yyyymmdd | reference date |
| HH | reference time |
| model | IFS |
| resol | 0p25 |
| stream [^1] | oper, enfo, waef, wave, scda, scwv |
| step [^1] | forecast time step |
| U | unit of the time step (h) |
| type [^1] | fc and ef |
| format | grib2 or bufr |
:::

The valid combinations are in detail described [here](https://confluence.ecmwf.int/display/DAC/ECMWF+open+data%3A+real-time+forecasts+from+IFS+and+AIFS).

## Index files
Each GRIB file has its corresponding index file which can be accessed by substituting the `.grib2` extension with `.index` in the URL. Each line in an index file represents a GRIB field in the corresponding GRIB file. It is described using the [MARS query language](https://confluence.ecmwf.int/display/WEBAPI/Brief+MARS+request+syntax). The keys `_offset`  and `_length` represent the byte offset and length of the corresponding field respectively. This allows us to download a single field from the GRIB file using HTTP [byte-range requests](https://www.keycdn.com/support/byte-range-requests), see [Retrieve Data](../datadownload/data-download.ipynb).
```
{"domain": "g", "date": "20250608", "time": "0000", "expver": "0001", "class": "od", "type": "fc", "stream": "oper", "step": "0", "levtype": "sfc", "param": "asn", "_offset": 0, "_length": 71895}
```

[^1]: Further information can be found in [Appendix](../appendix.md).