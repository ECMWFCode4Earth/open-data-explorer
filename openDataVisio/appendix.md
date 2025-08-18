# Appendix

## List of Identification Keywords
---

:::{table} Type and its corresponding values.
:label: tableType
:align: center

| Keyword | Description | Value | Long Name |
| -------- | ---- | -------- | ---- |
| type | Specifies the type of field. | fc | Forecast |
|  |  | ef | Ensemble forecast |
|  |  | cf | Control forecast  |
|  |  | pf | Perturbed forecast |
|  |  | ep | Event probability |
|  |  | tf | Trajectory forecast |
:::

## IFS
:::{table} Stream and its corresponding values of the IFS.
:label: tableStreamIFS
:align: center

| Keyword | Description | Value | Long Name | Reference Time |
| -------- | ---- | -------- | ---- | ---- |
| stream | Identifies the forecasting system used to generated the data when the same meteorological types are archived. | oper | Operational Atmospheric model (daily archive) | 00 and 12 UTC |
|  |  | enfo | Ensemble prediction system | 00, 06, 12, and 18 UTC |
|  |  | waef | Wave ensemble forecast | 00, 06, 12, and 18 UTC |
|  |  | wave | Wave model | 00 and 12 UTC |
|  |  | scda | Atmospheric model (short cutoff daily archive) | 06 and 18 UTC |
|  |  | scwv | Wave model (short cutoff) | 06 and 18 UTC |
:::

:::{table} Step and its corresponding values of the IFS.
:label: tableStepIFS
:align: center

| Keyword | Description | Forecasting System | Reference Time | List of Time Steps |
| -------- | ---- | -------- | ---- | ---- |
| step | The forecast time step in hours from the forecast base time. | Control Forecast | 00 and 12 UTC | from 0 to 144 by 3 and from 150 to 360 by 6 |
|  |  |  | 06 and 18 UTC | from 0 to 144 by 3 |
|  |  | Tropical cyclones tracks - HRES | 00 and 12 UTC | from 0 to 240 |
|  |  |  | 06 and 18 UTC | from 0 to 90 |
|  |  | ENS | 00 and 12 UTC | from 0 to 144 by 3 and from 150 to 360 by 6 |
|  |  |  | 06 and 18 UTC | from 0 to 144 by 3 |
|  |  | Tropical cyclones tracks - ENS | 00 and 12 UTC | from 0 to 360 |
|  |  |  | 06 and 18 UTC | from 0 to 144 |
|  |  | Probabilities, daily weather events | 00 and 12 UTC | 0-24 to 336-360 by 12 |
|  |  | Probabilities - atmosphere and wave |  | from 12 to 360 by 12 |
:::

## AIFS Single
:::{table} Stream and its corresponding values of the AIFS Single.
:label: tableStreamAIFSS
:align: center

| Keyword | Description | Value | Long Name | Reference Time |
| -------- | ---- | -------- | ---- | ---- |
| stream | Identifies the forecasting system used to generated the data when the same meteorological types are archived. | oper | Operational Atmospheric model (daily archive) | 00, 06, 12, and 18 UTC |
:::

:::{table} Step and its corresponding values of the AIFS Single.
:label: tableStepAIFSS
:align: center

| Keyword | Description | Forecasting System | Reference Time | List of Time Steps |
| -------- | ---- | -------- | ---- | ---- |
| step | The forecast time step in hours from the forecast base time. | Deterministic | 00, 06, 12, and 18 UTC | from 0 to 360 by 6 |
|  |  | Tropical cyclones tracks | 00, 06, 12, and 18 UTC | from 0 to 240 |
:::

### AIFS Ensemble
:::{table} Stream and its corresponding values of the AIFS Ensemble.
:label: tableStreamAIFSE
:align: center

| Keyword | Description | Value | Long Name | Reference Time |
| -------- | ---- | -------- | ---- | ---- |
| stream | Identifies the forecasting system used to generated the data when the same meteorological types are archived. | enfo | Ensemble prediction system  | 00, 06, 12, and 18 UTC |
:::

:::{table} Step and its corresponding values of the AIFS Ensemble.
:label: tableStepAIFSE
:align: center

| Keyword | Description | Forecasting System | Reference Time | List of Time Steps |
| -------- | ---- | -------- | ---- | ---- |
| step | The forecast time step in hours from the forecast base time. | ENS | 00, 06, 12, and 18 UTC | from 0 to 360 by 6 |
:::

:::{seealso}
All the keywords which can be used to retrieve real-time data are explained [here](https://confluence.ecmwf.int/display/UDOC/Keywords+in+MARS+and+Dissemination+requests).
:::
