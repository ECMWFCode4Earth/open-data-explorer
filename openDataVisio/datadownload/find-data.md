# ECMWF Open Data
---

Currently, open data are available from the following locations: [ECMWF Data Store (ECPDS)](https://data.ecmwf.int/forecasts/), [Amazon's AWS](https://aws.amazon.com/marketplace/pp/prodview-ykwikoqdzpamo?sr=0-1&ref_=beagle&applicationId=AWSMPContessa#resources), [Google Cloud](https://console.cloud.google.com/marketplace/product/bigquery-public-data/open-data-ecmwf), [Microsoft's Azure](https://planetarycomputer.microsoft.com/dataset/ecmwf-forecast), and [Open-meteo](https://open-meteo.com/).

## ECMWF Data Store (ECPDS)
It offers datasets from current date and up to four days before today.

:::{figure} ../images/ecmwf-data-store.png
:label: fig:ecmwfds
:::

## Amazon's AWS
It hosts data from 2023 to 2025.

:::{figure} ../images/aws.png
:label: fig:aws
:::
:::{figure} ../images/AWS_ecmwf_real-time_forecasts.png
:label: fig:aws_resources
:::

## Google Cloud
:::{figure} ../images/Google.png
:label: fig:google
:::

::::{margin}
:::{note}
To access open data within Google Cloud, you will need to authenticate using your Google account or [`gsutil`](https://cloud.google.com/storage/docs/gsutil) tool to access Cloud Storage from the command line.
:::
::::

## Microsoft Azure

It makes the ECMWF products available for the previous 30 days.

:::{figure} ../images/Microsoft.png
:label: fig:microsoft
:::

::::{margin}
:::{important}
To access data, users are required to utilise tokens created by the Data Authentication API. Public access is not permitted on every data sets. For more information, see the [Planetary Computer](https://planetarycomputer.microsoft.com/docs/concepts/sas/) documentation.
:::
::::

## Open-Meteo
With an open-source weather API one can access forecast data for up to 16 days or historical data from 2017 onwards.

:::{figure} ../images/open-meteo.png
:label: fig:openmeteo
:::

% ## [Oikolab](https://docs.oikolab.com/#global-datasets)
% Only IFS open data available.
% ```{warning}
% To retrieve open data, you will need to log into your account and then you will find your API key on the profile page.
% ```
% :::{figure} ../images/oikolab.png
% :label: fig:oikolab
% :::

:::{seealso}
For a full list of other locations, where you can find open data available, visit the [ECMWF open datasets](https://confluence.ecmwf.int/display/DAC/ECMWF+open+data%3A+real-time+forecasts+from+IFS+and+AIFS) website.
:::

:::{card}
1. Copyright Statement: Copyright "© 2025 European Centre for Medium-Range Weather Forecasts (ECMWF)".

2. Source: www.ecmwf.int

3. Licence Statement: This data is published under a Creative Commons Attribution 4.0 International (CC BY 4.0). https://creativecommons.org/licenses/by/4.0/

4. Disclaimer: ECMWF does not accept any liability whatsoever for any error or omission in the data, their availability, or for any loss or damage arising from their use.
:::