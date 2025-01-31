# Hazard datasets

The Copernicus Climate Change Service (C3S) Climate Data Store (CDS) provides access to a wide variety of climate-related data, including observational data from ground-based instruments, satellites and other sources, reanalysis data, and environmental and climate model projections.

Data in {abbr}`CDS (Climate Data Store)` follow strict quality control and guidance when it comes to the FAIR principle and metadata. The data can be accessed in various formats, such as netCDF, GRIB, and CSV, and can be used for a range of applications, including research, policy-making, and commercial activities.

Data in the {abbr}`CDS (Climate Data Store)` is available through the Climate Data Store __[Application Program Interface](https://cds.climate.copernicus.eu/how-to-api)__ (API) service.  Users need to sign up for an account on the {abbr}`CDS (Climate Data Store)` website and use the {abbr}`CDS (Climate Data Store)` API or the web interface to download the required data.

:::{tip}

Check with your local meteorological service!
:::



## General climate datasets

Quantities that characterize the Earth system.
Basic properties of the atmosphere like temperature, wind, and precipitation amounts.


### Observations

:::{dropdown} E-OBS (Europe, gridded)

Calculated from station data acquired through the network of the European Climate Assessment & Dataset (ECA&D) project. The observational data is gridded to regular latitude-longitude grid and is available at 0.1 and 0.25 degrees horizontal resolution. The dataset is daily, meaning the observations cover 24 hours per time step. Temporal coverage spans from 1950 to present. Available variables on daily basis: mean, minimum and maximum temperature, total precipitation, mean sea level pressure, mean wind speed at 10-meter height, mean relative humidity and surface shortwave downwelling radiation (i.e. solar radiation) measured at Earth’s surface. The dataset covers the European land areas: 25N-71.5N x 25W-45E.

The data files are in NetCDF-4 format and can be downloaded via {abbr}`C3S (Copernicus Climate Change Service)` {abbr}`CDS (Climate Data Store)` - __[E-OBS daily gridded meteorological data for Europe from 1950 to present derived from in-situ observations](https://cds.climate.copernicus.eu/datasets/insitu-gridded-observations-europe?tab=overview)__ and via __[ECA&D](https://www.ecad.eu/download/ensembles/download.php)__.
:::



### Reanalysis

Recreations of the state of the Earth system by a computer model under the consideration of available observations.
Not merely an interpolation between observations, but inclusion of scientific knowledge about processes in the atmosphere etc. as encoded in the model.

:::{figure} ../../images/hazard_image.png
:name: three-stages-of-reanalysis

The three stages of reanalysis; the amount of observational data used for the RA per area unit increases from the global to the surface reanalysis as indicated by the arrows. (Source: __[UERRA data user guide](https://datastore.copernicus-climate.eu/documents/uerra/D322_Lot1.4.1.2_User_guides_v3.3.pdf)__)
:::


:::{dropdown} ERA5

Global atmospheric reanalysis datasets produced by the European Centre for Medium-Range Weather Forecasts (ECMWF). Reanalysis combines model data with observations from across the world into a globally complete and consistent dataset using the laws of physics. ERA5 datasets provide a comprehensive view of the Earth's atmosphere, ocean and land-surface quantities with regular latitude-longitude grid available at 0.25 degrees horizontal resolution. Temporal coverage spans from 1950 to present and is updated daily with a latency of about 5 days. 

Temporal coverage spans from 1950 to present and is updated monthly with a delay of about three months relatively to actual date. Both, ERA5 and ERA5-Land, dataset are provided hourly. A large number of atmospheric, ocean-wave and land-surface quantities needed in {abbr}`CRA (Climate Risk Assessment)` can be downloaded via {abbr}`CDS (Climate Data Store)` both for both ERA5 - __[ERA5 hourly data on single levels from 1940 to present](https://cds.climate.copernicus.eu/datasets/reanalysis-era5-single-levels?tab=overview)__.

Both reanalysis data sets are widely used in climate research, weather forecasting, and other applications. ERA5 also includes an ensemble component at half the resolution to provide information on the synoptic uncertainty of its products.

- Temporal coverage: ...
- Resolution: ...
- Quality assessment: ...
- Data format: ...
- Access requirements: ...

How to access: cdsapi.
:::


:::{dropdown} ERA5-Land

ERA5-Land has enhanced horizontal resolution compared to ERA5, but it covers only land areas.
ERA5-Land is gridded to regular latitude-longitude grid and is available at 0.1 degrees horizontal resolution.
ERA5-land parameter uncertainty currently can be accessed using the equivalent ERA5 fields.


ERA-Land - [ERA5-Land hourly data from 1950 to present](https://cds.climate.copernicus.eu/datasets/reanalysis-era5-land?tab=overview).
:::



:::{dropdown} UERRA (Europe)

__[Uncertainties in Ensembles of Regional ReAnalysis](https://uerra.eu/)__

Reanalysis data of the atmosphere, the surface and near-surface as well as for the soil covering Europe. Climate variables are generated with the UERRA-HARMONIE and the MESCAN-SURFEX systems. The system uses global reanalysis data as lateral boundaries: ERA40 for the period 1961-1978, after that ERA-interim. UERRA uses a combination of advanced data assimilation techniques and high-resolution regional climate models to produce regional reanalysis at horizontal resolution of 11km (0.1 degrees). Temporal coverage spans from January 1961 to July 2019. The system provides analyses with 6-hour time step. Between the analyses, forecasts of the system are available with hourly resolution.

The data files are in GRIB or NetCDF-4 format and can be downloaded via {abbr}`C3S (Copernicus Climate Change Service)` {abbr}`CDS (Climate Data Store)` (Complete UERRA regional reanalysis for Europe from 1961 to 2019).

In addition to the standard atmospheric variables, UERRA also provides uncertainty estimates for each variable, which can be used to assess the reliability of the data and quantify the level of confidence in any climate-related analysis or decision-making process.
:::


### Climate Projections

Data from climate model simulations.
Direct and bias-corrected.
Runs often started in the past, provide not just future projection but also consistent dataset to represent the present climate.


:::{dropdown} CMIP5 and CMIP6

Global climate model simulations produced by international research institutions as part of the Coupled Model Intercomparison Project (CMIP). The datasets provide daily and monthly projections of historical periods and future climate change from a large number of experiments and models under different scenarios of greenhouse gas emissions. Data is gridded to regular latitude-longitude grid with horizontal resolution of 0.125° x 0.125° to 5° x 5° depending on the model. CMIP5 and CMIP6 data covers the period from 1850 to 2100, including the historical runs for 1950-2005 (CMIP5) and 1950-2014 (CMIP6). Climate projection experiments follow the combined pathways of Shared Socioeconomic Pathway (SSP, CMIP6) and Representative Concentration Pathway (RCP, CMIP5 and CMIP6). The SSP and RCP scenarios provide different pathways of the future climate forcing.

Both CMIP5 and CMIP6 data files are in NetCDF-4 format and can be downloaded via {abbr}`C3S (Copernicus Climate Change Service)` {abbr}`CDS (Climate Data Store)`: __[CMIP5 daily data on single levels](https://cds.climate.copernicus.eu/datasets/projections-cmip5-daily-single-levels?tab=overview)__ and [CMIP6 climate projections](https://cds.climate.copernicus.eu/datasets/projections-cmip6?tab=overview).
:::


:::{dropdown} EURO-CORDEX regional climate data

High-resolution regional climate model simulations for Europe, produced by a consortium of European research institutions. The dataset provides projections of future climate change at a regional scale, with a resolution of 12.5 km. EURO-CORDEX data covers the period from 1950 to 2100, including the historical runs for 1950-2005. The CORDEX experiments are using the RCP 2.6, 4.5 and 8.5 scenarios providing different pathways of the future climate forcing.

The datasets can be accessed from {abbr}`C3S (Copernicus Climate Change Service)` {abbr}`CDS (Climate Data Store)` __[CORDEX regional climate model data on single levels](https://cds.climate.copernicus.eu/datasets/projections-cordex-domains-single-levels?tab=overview)__ and they are widely used in climate research, impact assessments, and adaptation planning at the regional level.
:::



## Hazard-specific datasets

Datasets with pre-processing, event selection, additional modelling applied.


### Floods

:::{dropdown} JRC European flood hazard maps

Flood hazard maps.

- Coverage: Europe + Mediterranean basin
- Documentation: 

Example usage: River floods hazard assessment.
:::


:::{dropdown} JRC Global river flood hazard maps
:name: dataset-jrc-global-river-flood-hazard-maps

Inundation along the river network, for seven different flood return periods (from 1-in-10-years to 1-in-500-years). Modelled with LISFLOOD and LISFLOOD-FP.

Dataset
: [JRC Global river flood hazard maps](http://data.europa.eu/89h/jrc-floods-floodmapgl_rp50y-tif)

Coverage
: global, except Greenland and Antarctica and small islands with river basins smaller than 500 km².

Resolution
: 90 m (3 arcseconds).

Format
: GeoTIFF
:::


### Heavy Rainfall


### Droughts


### Heatwaves


### Fire

:::{dropdown} Fire Weather Index from temperature- and precipitation-perturbed historical scenarios (Europe)

...
:::


### Snow


### Wind

