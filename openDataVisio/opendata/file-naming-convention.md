# File-naming convention on real-time data
---

ECMWF products, used and analysed in this handbook, are encoded in [WMO FM-92 GRIB edition 2](https://codes.wmo.int/codeform/_grib2) excluding Tropical Cyclones. The latter is encoded in [WMO FM-94 BUFR](https://codes.wmo.int/codeform/_bufr4) format.

:::{seealso}
The [File-naming convention and format](https://confluence.ecmwf.int/display/DAC/File+naming+convention+and+format+for+real-time+data#Filenamingconventionandformatforrealtimedata-Naming-AIFSviadissemination) provides valuable information about different file-naming convention templates for real-time products.
:::

::::{margin}
:::{note}
To learn more about where to find data, visit [ECMWF Open Data](../datadownload/find-data.ipynb) website.
:::
::::

## Technical details
::::{margin}
:::{attention}
There is a distinction between IFS and AIFS in the ending of the file names and the available types. 
:::
::::

### IFS Data
IFS open data products are available at 0.25 degrees resolution, one hour after the [real-time dissemination schedule](https://confluence.ecmwf.int/display/DAC/Dissemination+schedule). The file names are following this naming convention: `ROOT`/`yyyymmdd`/`HH`z/`model`/`resol`/`stream`/`yyyymmdd` `HH`0000-`step` `U`-`stream`-`type`.`format`.

:::{table} File-naming convention of the ECMWF IFS model outputs. [^1]
:label: tableIFS
:align: center

| File-naming convention | Values |
| -------- | ---- |
| ROOT | URL of a site hosting the open data |
| yyyymmdd | reference date |
| HH | reference time |
| model | ifs |
| resol | 0p25 |
| stream | oper, enfo, waef, wave, scda, scwv |
| step | forecast time step |
| U | unit of the time step (h) |
| type | fc, ef (cf, pf), ep, and tc |
| format | grib2 or bufr |
:::

Both types `cf` and `pf` are included in the files with `type=ef`. <br>

:::{seealso}
The valid combinations are in detail described [here](https://confluence.ecmwf.int/display/DAC/ECMWF+open+data%3A+real-time+forecasts+from+IFS+and+AIFS).
:::

### AIFS Single Data
AIFS open data products are released as soon as the data are generated. These data are also produced at 0.25 degrees resolution.

:::{table} File-naming convention of the ECMWF AIFS model outputs. [^1]
:label: tableAIFS
:align: center

| File-naming convention | Values |
| -------- | ---- |
| ROOT | URL of a site hosting the open data |
| yyyymmdd | reference date |
| HH | reference time |
| model | aifs-single |
| resol | 0p25 |
| stream | oper |
| step | forecast time step |
| U | unit of the time step (h) |
| type | fc and tc|
| format | grib2 or bufr |
:::

### AIFS Ensemble Data
The same as for the AIFS open data products apply to the AIFS ENS.

:::{table} File-naming convention of the ECMWF AIFS ENS model outputs. [^1]
:label: tableAIFSens
:align: center

| File-naming convention | Values |
| -------- | ---- |
| ROOT | URL of a site hosting the open data |
| yyyymmdd | reference date |
| HH | reference time |
| model | aifs-ens |
| resol | 0p25 |
| stream | enfo |
| step | forecast time step |
| U | unit of the time step (h) |
| type | cf, pf, and ep |
| format | grib2 or bufr |
:::

::::{margin}
:::{important}
AIFS data predicting event probabilities (`type=ep`) include all the steps in a file (`step=360`).
:::
::::

## Index files
Each GRIB file has its corresponding index file which can be accessed by substituting the `.grib2` extension with `.index` in the URL. Each line in an index file represents a GRIB field in the corresponding GRIB file. It is described using the [MARS query language](https://confluence.ecmwf.int/display/WEBAPI/Brief+MARS+request+syntax). The keys `_offset`  and `_length` represent the byte offset and length of the corresponding field respectively. This allows us to download a single field from the GRIB file using HTTP [byte-range requests](https://www.keycdn.com/support/byte-range-requests), see [Retrieve Data](../datadownload/data-download.ipynb). <br>

Files with the `type=ep` contain ensemble means and standard deviations as well as probabilities datasets.<br>

The examples below show a line extracted from an index file of the:
- IFS:
```
{"domain": "g", "date": "20250608", "time": "0000", "expver": "0001", "class": "od", "type": "fc", "stream": "oper", "levtype": "sfc", "step": "0", "param": "tp", "_offset": 14804835, "_length": 224}
```
- AIFS:
::::{margin}
:::{attention}
Note the value of the `class` keyword which is `ai` in the case of the AIFS model. This value indicates the operational AIFS products and the `od` represents the operational archive.
:::
::::

```
{"domain": "g", "date": "20250608", "time": "0000", "expver": "0001", "class": "ai", "type": "fc", "stream": "oper", "step": "0", "levtype": "sfc", "param": "100v", "_offset": 0, "_length": 1382370}
```
- AIFS ENS:
```
{"domain": "g", "date": "20250803", "time": "0000", "expver": "0001", "class": "ai", "type": "cf", "stream": "enfo", "step": "0", "levtype": "sfc", "param": "2t", "model": "aifs-ens", "_offset": 61637992, "_length": 618016}
```
:::{important}
Index files of the AIFS ENS products have the additional parameter `model`.
:::

[^1]: Further information can be found in the [Appendix](../appendix.md).
