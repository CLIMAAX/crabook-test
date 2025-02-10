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

:::{dropdown} E-OBS

Calculated from station data acquired through the network of the European Climate Assessment & Dataset (ECA&D) project. The observational data is gridded to regular latitude-longitude grid and is available at 0.1 and 0.25 degrees horizontal resolution. The dataset is daily, meaning the observations cover 24 hours per time step. Temporal coverage spans from 1950 to present. Available variables on daily basis: mean, minimum and maximum temperature, total precipitation, mean sea level pressure, mean wind speed at 10-meter height, mean relative humidity and surface shortwave downwelling radiation (i.e. solar radiation) measured at Earth’s surface. The dataset covers the European land areas: 25N-71.5N x 25W-45E.

The data files are in NetCDF-4 format and can be downloaded via {abbr}`C3S (Copernicus Climate Change Service)` {abbr}`CDS (Climate Data Store)` - __[E-OBS daily gridded meteorological data for Europe from 1950 to present derived from in-situ observations](https://cds.climate.copernicus.eu/datasets/insitu-gridded-observations-europe?tab=overview)__ and via __[ECA&D](https://www.ecad.eu/download/ensembles/download.php)__.

Dataset
: ...

Spatial coverage
: Europe; gridded
:::


:::{dropdown} CHIRPS

https://www.chc.ucsb.edu/data/chirps

Precipitation.
:::


### Reanalysis

Recreations of the state of the Earth system by a computer model under the consideration of available observations.
Reanalysis combines model data with observations into a complete and consistent dataset using the laws of physics.
Not merely an interpolation between observations, but inclusion of scientific knowledge about processes in the atmosphere etc. as encoded in the model.

:::{figure} ../../images/hazard_image.png
:figclass: margin-caption
:name: three-stages-of-reanalysis

The three stages of reanalysis; the amount of observational data used for the RA per area unit increases from the global to the surface reanalysis as indicated by the arrows. (Source: __[UERRA data user guide](https://datastore.copernicus-climate.eu/documents/uerra/D322_Lot1.4.1.2_User_guides_v3.3.pdf)__)
:::


{numref}`three-stages-of-reanalysis` shows different types of reanalysis and their relationship.
Global reanalysis from global weather models.
Limited-area models nested inside global models to refine reanalysis data for a specific region.
Surface reanalysis based on models of the surface, with global or regional reanalysis data driving the surface model.
From global to regional to surface, resolution and use of observations generally increases.


:::{dropdown} ERA5

Atmospheric reanalysis dataset produced by the European Centre for Medium-Range Weather Forecasts (ECMWF), widely used in climate research, weather forecasting, and other applications.
Includes an ensemble component at half the resolution to provide information on synoptic uncertainty.

Dataset
: [hourly data on single levels](https://doi.org/10.24381/cds.adbb2d47),
  [hourly data on pressure levels](https://doi.org/10.24381/cds.bd0915c6)

Temporal coverage
: 1940 to present (regularly updated)

Spatial coverage
: global

Resolution
: 0.25° horizontal

Format
: GRIB, NetCDF

Access requirements
: ECMWF account for CDS

In workflows
: <img src="../../images/icon_s/icon_s_snow.png" alt="" class="hazard-icon"> [Heavy snowfall and blizzards](../../notebooks/workflows/SNOW/01_Heavy_snowfall_and_blizzards/Risk_workflow_description_SNOW_BLIZZARDS),
  <img src="../../images/icon_s/icon_s_wind.png" alt="" class="hazard-icon"> [Windstorm](../../notebooks/workflows/STORMS/01_windstorm/Risk_workflow_description_STORMS)
:::


:::{dropdown} ERA5-Land

ERA5-Land has enhanced horizontal resolution compared to ERA5, but it covers only land areas.
ERA5-Land is gridded to regular latitude-longitude grid and is available at 0.1 degrees horizontal resolution.
ERA5-land parameter uncertainty currently can be accessed using the equivalent ERA5 fields.


ERA-Land - [ERA5-Land hourly data from 1950 to present](https://cds.climate.copernicus.eu/datasets/reanalysis-era5-land?tab=overview).
:::



:::{dropdown} UERRA

__[Uncertainties in Ensembles of Regional ReAnalysis](https://uerra.eu/)__

Reanalysis data of the atmosphere, the surface and near-surface as well as for the soil covering Europe. Climate variables are generated with the UERRA-HARMONIE and the MESCAN-SURFEX systems. The system uses global reanalysis data as lateral boundaries: ERA40 for the period 1961-1978, after that ERA-interim. UERRA uses a combination of advanced data assimilation techniques and high-resolution regional climate models to produce regional reanalysis at horizontal resolution of 11km (0.1 degrees). Temporal coverage spans from January 1961 to July 2019. The system provides analyses with 6-hour time step. Between the analyses, forecasts of the system are available with hourly resolution.

The data files are in GRIB or NetCDF-4 format and can be downloaded via {abbr}`C3S (Copernicus Climate Change Service)` {abbr}`CDS (Climate Data Store)` (Complete UERRA regional reanalysis for Europe from 1961 to 2019).

In addition to the standard atmospheric variables, UERRA also provides uncertainty estimates for each variable, which can be used to assess the reliability of the data and quantify the level of confidence in any climate-related analysis or decision-making process.
:::


### Climate Projections

Data from climate model simulations.
Direct and bias-corrected.
Runs often started in the past, provide not just future projection but also consistent dataset to represent the present climate.


:::{dropdown} CMIP5

Global climate model simulations produced by international research institutions as part of the Coupled Model Intercomparison Project (CMIP). The datasets provide daily and monthly projections of historical periods and future climate change from a large number of experiments and models under different scenarios of greenhouse gas emissions. Data is gridded to regular latitude-longitude grid with horizontal resolution of 0.125° x 0.125° to 5° x 5° depending on the model. CMIP5 and CMIP6 data covers the period from 1850 to 2100, including the historical runs for 1950-2005 (CMIP5) and 1950-2014 (CMIP6). Climate projection experiments follow the combined pathways of Shared Socioeconomic Pathway (SSP, CMIP6) and Representative Concentration Pathway (RCP, CMIP5 and CMIP6). The SSP and RCP scenarios provide different pathways of the future climate forcing.

Both CMIP5 and CMIP6 data files are in NetCDF-4 format and can be downloaded via {abbr}`C3S (Copernicus Climate Change Service)` {abbr}`CDS (Climate Data Store)`: __[CMIP5 daily data on single levels](https://cds.climate.copernicus.eu/datasets/projections-cmip5-daily-single-levels?tab=overview)__ and [CMIP6 climate projections](https://cds.climate.copernicus.eu/datasets/projections-cmip6?tab=overview).
:::


:::{dropdown} CMIP6

Global climate model simulations produced by international research institutions as part of the Coupled Model Intercomparison Project (CMIP). The datasets provide daily and monthly projections of historical periods and future climate change from a large number of experiments and models under different scenarios of greenhouse gas emissions. Data is gridded to regular latitude-longitude grid with horizontal resolution of 0.125° x 0.125° to 5° x 5° depending on the model. CMIP5 and CMIP6 data covers the period from 1850 to 2100, including the historical runs for 1950-2005 (CMIP5) and 1950-2014 (CMIP6). Climate projection experiments follow the combined pathways of Shared Socioeconomic Pathway (SSP, CMIP6) and Representative Concentration Pathway (RCP, CMIP5 and CMIP6). The SSP and RCP scenarios provide different pathways of the future climate forcing.

Both CMIP5 and CMIP6 data files are in NetCDF-4 format and can be downloaded via {abbr}`C3S (Copernicus Climate Change Service)` {abbr}`CDS (Climate Data Store)`: __[CMIP5 daily data on single levels](https://cds.climate.copernicus.eu/datasets/projections-cmip5-daily-single-levels?tab=overview)__ and [CMIP6 climate projections](https://cds.climate.copernicus.eu/datasets/projections-cmip6?tab=overview).
:::


:::{dropdown} CORDEX: Coordinated Regional Climate Downscaling Experiment

High-resolution regional climate model simulations for Europe, produced by a consortium of European research institutions. The dataset provides projections of future climate change at a regional scale, with a resolution of 12.5 km. EURO-CORDEX data covers the period from 1950 to 2100, including the historical runs for 1950-2005. The datasets are widely used in climate research, impact assessments, and adaptation planning at the regional level.

Dataset
: https://doi.org/10.24381/cds.bc91edc3

Temporal coverage
: TODO

Scenarios
: RCP 2.6, 4.5 and 8.5 (availability varies with domain and model)

Spatial coverage
: See https://cordex.org/domains/

Format
: NetCDF

Access requirements
: ECMWF account for CDS

In workflows
: <img src="../../images/icon_s/icon_s_heavy_rainfall.png" alt="" class="hazard-icon"> [Extreme precipitation](../../notebooks/workflows/HEAVY_RAINFALL/01_Extreme_precipitation/Extreme_precipitation_Intro),
  <img src="../../images/icon_s/icon_s_heatwaves.png" alt="" class="hazard-icon"> [Urban heatwaves](../../notebooks/workflows/HEATWAVES/01_Urban_heatwaves/heatwave_intro),
  <img src="../../images/icon_s/icon_s_droughts.png" alt="" class="hazard-icon"> [Agricultural drought](../../notebooks/workflows/DROUGHTS/02_agriculture_drought/AGRICULTURE_Risk_workflow_description),
  <img src="../../images/icon_s/icon_s_snow.png" alt="" class="hazard-icon"> [Heavy snowfall & blizzards](../../notebooks/workflows/SNOW/01_Heavy_snowfall_and_blizzards/Risk_workflow_description_SNOW_BLIZZARDS)
:::


:::{dropdown} ISIMIP3b: bias-adjusted atmospheric climate input data

TODO

Dataset
: TODO

In workflows
: <img src="../../images/icon_s/icon_s_droughts.png" alt="" class="hazard-icon"> [Relative drought](../../notebooks/workflows/DROUGHTS/01_relative_drought/Risk_workflow_description_RELATIVE_DROUGHT)
:::


:::{dropdown} ECLIPS-2.0: bias-corrected EURO-CORDEX

TODO

Dataset
: https://doi.org/10.5281/zenodo.3952159

In workflows
: <img src="../../images/icon_s/icon_s_fire.png" alt="" class="hazard-icon"> [Wildfire (ML approach)](../../notebooks/workflows/FIRE/01_wildfire_ML/Risk_workflow_description_FIRE_ML)
:::


:::{dropdown} CHELSA: Climatologies at high resolution for the earth’s land surface areas

TODO

Dataset
: https://chelsa-climate.org/

In workflows
: <img src="../../images/icon_s/icon_s_fire.png" alt="" class="hazard-icon"> [Wildfire (ML approach)](../../notebooks/workflows/FIRE/01_wildfire_ML/Risk_workflow_description_FIRE_ML)
:::


## Hazard-specific datasets

Datasets with pre-processing, event selection, additional modelling applied.


### <img src="../../images/icon_s/icon_s_floods.png" alt="" class="hazard-icon"> Floods

:::{dropdown} JRC river flood hazard maps for Europe and the Mediterranean Basin region

Gridded inundation depth (in m) along the river network, for nine different flood return periods (from 1-in-10-years to 1-in-500-years).

Dataset
: http://data.europa.eu/89h/1d128b6c-a4ee-4858-9e34-6210707f3c81

Spatial coverage
: Most of geographical Europe and all the river basins entering the Mediterranean and Black Seas in the Caucasus, Middle East and Northern Africa countries.
  River basins > 150 km².

Format
: GeoTIFF

In workflows
: <img src="../../images/icon_s/icon_s_floods.png" alt="" class="hazard-icon"> [River floods](../../notebooks/workflows/FLOODS/02_River_flooding/FLOOD_RIVER_intro),
  <img src="../../images/icon_s/icon_s_floods.png" alt="" class="hazard-icon"> [Flood building damage and population exposed](03_Flood_damage_and_population_exposure/Risk_workflow_description_FLOOD_BUILDING_POPULATION)
:::


:::{dropdown} JRC global river flood hazard maps
:name: dataset-jrc-global-river-flood-hazard-maps

Gridded inundation depth (in m) along the river network, for seven different flood return periods (from 1-in-10-years to 1-in-500-years).

Dataset
: http://data.europa.eu/89h/jrc-floods-floodmapgl_rp50y-tif

Spatial coverage
: Global, except Greenland and Antarctica and small islands with river basins smaller than 500 km²

Resolution
: 90 m (3 arcseconds)

Format
: GeoTIFF
:::


:::{dropdown} WRI Aqueduct Floods Hazard Maps

Dataset
: https://www.wri.org/data/aqueduct-floods-hazard-maps

Documentation
: https://www.wri.org/research/aqueduct-floods-methodology

Temporal coverage
: 2010, 2030, 2050, 2080

Scenarios
: RCP4.5/SSP2, RCP8.5/SSP2, RCP8.5/SSP3

Spatial coverage
: global

Resolution
: 30'' x 30'' horizontal

Format
: GeoTIFF

In workflows
: <img src="../../images/icon_s/icon_s_floods.png" alt="" class="hazard-icon"> [River floods](../../notebooks/workflows/FLOODS/02_River_flooding/FLOOD_RIVER_intro)
:::


:::{dropdown} Deltares Global Flood Maps

Inundation maps of flood depth.

Dataset
: https://planetarycomputer.microsoft.com/dataset/deltares-floods

Spatial coverage
: global

Format
: Zarr, NetCDF

In workflows
: <img src="../../images/icon_s/icon_s_floods.png" alt="" class="hazard-icon"> [Coastal floods](../../notebooks/workflows/FLOODS/01_Coastal_flooding/Risk_workflow_description_FLOOD_COASTAL)
:::


:::{dropdown} Global sea level change indicators from 1950 to 2050 derived from reanalysis and high resolution CMIP6 climate projections

Statistical indicators of tides, storm surges and sea level that can be used to characterize global sea level in present-day conditions and also to assess changes under climate change.

Dataset
: https://doi.org/10.24381/cds.6edf04e0

Temporal coverage
: 1950 to 2050

Scenarios
: SSP5-8.5

Spatial coverage
: global

In workflows
: <img src="../../images/icon_s/icon_s_floods.png" alt="" class="hazard-icon"> [Coastal floods](../../notebooks/workflows/FLOODS/01_Coastal_flooding/Risk_workflow_description_FLOOD_COASTAL)
:::


:::{dropdown} IPCC 6th Assessment Report Sea Level Projections

Sea-level projections associated with the Intergovernmental Panel on Climate Change Sixth Assessment Report.

Dataset
: [Zenodo](https://doi.org/10.5281/zenodo.5914709), [NASA Sea Level Projection Tool](https://sealevel.nasa.gov/ipcc-ar6-sea-level-projection-tool)

Spatial coverage
: global

Format
: NetCDF

In workflows
: <img src="../../images/icon_s/icon_s_floods.png" alt="" class="hazard-icon"> [Coastal floods](../../notebooks/workflows/FLOODS/01_Coastal_flooding/Risk_workflow_description_FLOOD_COASTAL)
:::


### <img src="../../images/icon_s/icon_s_heatwaves.png" alt="" class="hazard-icon"> Heatwaves

:::{dropdown} Heat waves and cold spells in Europe derived from climate projections

Number of hot and cold spell days using different European-wide and national/regional definitions developed within the C3S European Health service.

Dataset
: https://doi.org/10.24381/cds.9e7ca677

Temporal coverage
: 1986 to 2085

Spatial coverage
: European region (approx. 27°N–72°N and 22°W–45°E)

Resolution
: 0.1° x 0.1° regular latitude-longitude grid

Format
: NetCDF

In workflows
: <img src="../../images/icon_s/icon_s_heatwaves.png" alt="" class="hazard-icon"> [Urban heatwaves](../../notebooks/workflows/HEATWAVES/01_Urban_heatwaves/heatwave_intro)
:::


:::{dropdown} Online Global Land Surface Temperature Estimation from Landsat 

Dataset
: https://rslab.gr/Landsat_LST.html

Temporal coverage
: past; depends on satellite

Spatial coverage
: global

Format
: GeoTIFF

In workflows
: <img src="../../images/icon_s/icon_s_heatwaves.png" alt="" class="hazard-icon"> [Urban heatwaves](../../notebooks/workflows/HEATWAVES/01_Urban_heatwaves/heatwave_intro)
:::


### <img src="../../images/icon_s/icon_s_fire.png" alt="" class="hazard-icon"> Fire

:::{dropdown} Fire danger indicators for Europe from 1970 to 2098 derived from climate projections

Projections of fire danger indicators for Europe based upon the Canadian Fire Weather Index System (FWI) under future climate conditions

Dataset
: https://doi.org/10.24381/cds.ca755de7

Temporal coverage
: 1970 to 2098

Spatial coverage
: Europe

Spatial resolution
: 0.11° x 0.11° horizontal

Format
: NetCDF

In workflows
: <img src="../../images/icon_s/icon_s_fire.png" alt="" class="hazard-icon"> [Wildfire (FWI)](../../notebooks/workflows/FIRE/02_wildfire_FWI/FWI_Risk_Description)
:::


:::{dropdown} 30-Year Canadian Fire Weather Index Simulations over Europe: CMIP6-Informed Temperature and Precipitation Perturbations

30-year Canadian Fire Weather Index (FWI), generated using the Global ECMWF Fire Forecast model, forced by ERA5 reanalysis data (1981-2010). Simulations incorporate perturbations in temperature and precipitation forcings based on CMIP6 climate projections under the SSP2-4.5 medium mitigation scenario. 

Dataset
: https://doi.org/10.5281/zenodo.10458185

Temporal coverage
: 1981 to 2010

Spatial coverage
: Europe (geographical)

Resolution
: 31 km horizontal

Format
: GRIB
:::


### <img src="../../images/icon_s/icon_s_wind.png" alt="" class="hazard-icon"> Wind

:::{dropdown} Winter windstorm indicators for Europe from 1979 to 2021 derived from reanalysis

Climatological indicators on European winter windstorms and their economic impact derived from ERA5 reanalysis.

Dataset
: https://doi.org/10.24381/cds.9b4ea013

Temporal coverage
: 1979 to 2021; October to March

Spatial coverage
: 20°W-35°E, 35°N-70°N

Resolution
: 1 km horizontal

Format
: NetCDF

In workflows
: <img src="../../images/icon_s/icon_s_wind.png" alt="" class="hazard-icon"> [Windstorm](../../notebooks/workflows/STORMS/01_windstorm/Risk_workflow_description_STORMS)
:::
