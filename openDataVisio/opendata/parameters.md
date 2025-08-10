# Parameters and Levels
---

Atmospheric fields can be specified on pressure levels or on a single level.

:::{table} Parameters available on pressure levels (hPa): 1000, 925, 850, 700, 600, 500, 400, 300, 250, 200, 150, 100, and 50.
:label: tableParamPressure
:align: center

| Parameter | Long Name | Units |
| -------- | ---- | ---- |
| d | Divergence | s$^{-1}$ |
| gh | Geopotential height | gpm |
| q | Specific humidity | kg/kg |
| r | Relative humidity | % |
| t | Temperature | K |
| u | U component of wind | m/s |
| v | V component of wind | m/s |
| w | Vertical velocity | m/s |
| vo | Vorticity (relative) | s$^{-1}$ |
:::

:::{note}
Only the principal parameters are listed in the table below. For more information, visit the [Parameter Database](https://codes.ecmwf.int/grib/param-db/) website.
:::

:::{table} Parameters available on a single level.
:label: tableParamSingle
:align: center

| Parameter | Long Name | Units |
| -------- | ---- | ---- |
| 10u |	10 metre U wind component | m/s |
| 10v |	10 metre V wind component | m/s |
| 100u | 100 metre U wind component | m/s |
| 100v | 100 metre V wind component | m/s |
| 2t | 2 metre temperature | K |
| 2d | 2 metre dewpoint temperature| K |
| msl |	Mean sea level pressure | Pa |
| tp |	Total Precipitation | m |
| sp |	Surface pressure | Pa |
| st | Soil temperature | K |
:::