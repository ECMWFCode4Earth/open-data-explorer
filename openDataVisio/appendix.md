# Appendix

## List of Identification Keywords
---

:::{table} Stream and its corresponding values.
:label: tableStream
:align: center

| Keyword | Description |
| -------- | ---- |
| stream | Identifies the forecasting system used to generated the data when the same meteorological types are archived. |

| Value | Long Name | Reference Time |
| -------- | ---- | ---- |
| oper | Operational Atmospheric model (daily archive) | 00 and 12 UTC |
| enfo | Ensemble prediction system  |
| waef | Wave ensemble forecast |
| wave | Wave model | 00 and 12 UTC |
| scda | Atmospheric model (short cutoff daily archive) | 06 and 18 UTC |
| scwv | Wave model (short cutoff) | 06 and 18 UTC |
:::

:::{table} Step and its corresponding values.
:label: tableStep
:align: center

| Keyword | Description |
| -------- | ---- |
| step | The forecast time step in hours from the forecast base time. |

| Forecasting System | Reference Time | List of Time Steps |
| -------- | ---- | ---- |
| HRES | 00 and 12 UTC | from 0 to 144 by 3 and from 150 to 360 by 6 |
|  | 06 and 18 UTC | from 0 to 144 by 3 |
| ENS | 00 and 12 UTC | from 0 to 144 by 3 and from 150 to 360 by 6 |
|  | 06 and 18 UTC | from 0 to 144 by 3 |
:::

:::{table} Type and its corresponding values.
:label: tableType
:align: center

| Keyword | Description |
| -------- | ---- |
| type | Specifies the type of field. |

| Value | Long Name |
| -------- | ---- |
| fc | Forecast |
| ef | Errors in first guess  |
:::

:::{seealso}
All of the keywords which can be used to retrieve real-time data are explained [here](https://confluence.ecmwf.int/display/UDOC/Keywords+in+MARS+and+Dissemination+requests).
:::
