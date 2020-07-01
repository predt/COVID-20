# Unified COVID-19 Dataset
[![Copyright: © 2020 JHU)](https://img.shields.io/badge/Copyright-%C2%A9%202020%20JHU-blue.svg)](https://pages.jh.edu/~hbadr1)
[![Credits: NASA](https://img.shields.io/badge/Credits-NASA-blue.svg)](#Credits)
[![Citation: Badr et. al 2020](https://img.shields.io/badge/Citation-Badr%20et%20al.%202020-blue.svg)](#Citation)
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![GitHub Commit](https://img.shields.io/github/last-commit/hsbadr/COVID-19)](https://github.com/hsbadr/COVID-19/commits/master)

This is an all-in-one unified COVID-19 dataset to fulfil the following objectives:
  * Mapping all geospatial units globally into a unique standardized ID.
  * Standardizing administrative names and codes at all levels.
  * Standardizing dates, data types, and formats.
  * Unifying variable names, types, and categories.
  * Merging data from all credible sources at all levels.
  * Cleaning the data and fixing confusing entries.
  * Integrating hydrometeorological variables at all levels.
  * Integrating an augmented version from all sources (*future releases*).
  * Optimizing the data for machine learning applications.

## Geospatial ID

<img src="https://pages.jh.edu/~hbadr1/files/COVID-19_ID.svg#6" title="Geospatial ID for the Unified COVID-19 Dataset" alt="COVID-19 ID" style="display: block; margin: auto;" />

## Lookup Table

|     Column         |    Type    |              Description            |
|:------------------:|:----------:|:------------------------------------|
| **ID**             | Charachter | Geospatial ID, unique identifier (described above) |
| **Admin0**         | Charachter | Standard name of administrative level 0 (countries) |
| **Admin1**         | Charachter | Standard name of administrative level 1 (e.g., provinces, states, groups of regions) |
| **Admin2**         | Charachter | Standard name of administrative level 2 (e.g., counties and regions) |
| **Admin3**         | Charachter | Standard name of administrative level 3 (e.g., districts and ZTCA) |
| **Level**          | Charachter | Geospatial level (e.g., Country, Province, State, County, District, and NUTS 0-3) |
| **ISO1_3N**        | Charachter | ISO 3166-1 numeric code, 3-digit, administrative level 0 (countries) |
| **ISO1_3C**        | Charachter | ISO 3166-1 alpha-3 code, 3-letter, administrative level 0 (countries) |
| **ISO1_2C**        | Charachter | ISO 3166-1 alpha-2 code, 2-letter, administrative level 0 (countries) |
| **ISO2**           | Charachter | ISO 3166-2 code, principal subdivisions (e.g., provinces and states) |
| **ISO2_UID**       | Charachter | ISO 3166-2 code, principal subdivisions (e.g., provinces and states), full/unique ID |
| **FIPS**           | Charachter | Federal Information Processing Standard (FIPS, United States) |
| **NUTS**           | Charachter | Nomenclature of Territorial Units for Statistics (NUTS, Europe) |
| **AGS**            | Charachter | Official municipality key / Amtlicher Gemeindeschlüssel (AGS, German regions only) |
| **ZTCA**           | Charachter | ZIP Code Tabulation Area (ZCTA, United States) |
| **Longitude**      | Double     | Geospatial coordinate (centroid), east–west |
| **Latitude**       | Double     | Geospatial coordinate (centroid), north–south |
| **Population**     | Integer    | Total population of each geospatial unit |

## Data Structure

|     Column         |    Type    |              Description            |
|:------------------:|:----------:|:------------------------------------|
| **ID**             | Charachter | Geospatial ID, unique identifier (described above) |
| **Date**           | Date       | Date of data record |
| **Cases**          | Integer    | Number of cumulative cases |
| **Cases_New**      | Integer    | Number of new daily cases |
| **Type**           | Charachter | Type of the reported cases |
| **Age**            | Charachter | Age group of the reported cases |
| **Sex**            | Charachter | Sex/gender of the reported cases |
| **Source**         | Charachter | Source of the data: CTP, JHU, NYC, NYT, DPC, RKI |

## Case Types

|        Type          |    Description   |
|:--------------------:|:-----------------|
| **Active**           | Active cases |
| **Confirmed**        | Confimed cases |
| **Deaths**           | Deaths |
| **Home_Confinement** | Home confinement / isolation |
| **Hospitalized**     | Total hospitalized cases excluding intensive care units |
| **Hospitalized_Now** | Currently hospitalized cases excluding intensive care units |
| **Hospitalized_Sym** | Symptomatic hospitalized cases excluding intensive care units |
| **ICU**              | Total cases in intensive care units |
| **ICU_Now**          | Currently in intensive care units |
| **Negative**         | Negative tests |
| **Pending**          | Pending tests |
| **Positive**         | Positive tests, including hospitalised cases and home confinement |
| **Positive_Dx**      | Positive cases emerged from clinical activity / diagnostics |
| **Positive_Sc**      | Positive cases emerging from surveys and tests |
| **Recovered**        | Recovered cases |
| **Tested**           | Cases tested = Tests - Pending |
| **Tests**            | Total performed tests |
| **Ventilator**       | Total cases receiving mechanical ventilation |
| **Ventilator_Now**   | Currently receiving mechanical ventilation |

## Data Sources

| Source  |    Description   |    Level    |
|:-------:|:-----------------|:------------|
| **JHU** | [Johns Hopkins University CSSE](https://github.com/CSSEGISandData/COVID-19) | Global & County/State, United States |
| **CTP** | [The COVID Tracking Project](https://covidtracking.com) | State, United States |
| **NYC** | [New York City Department of Health and Mental Hygiene](https://github.com/nychealth/coronavirus-data) | ZCTA/Borough, New York City |
| **NYT** | [The New York Times](https://github.com/nytimes/covid-19-data) | County/State, United States |
| **DPC** | [Italian Civil Protection Department](https://github.com/pcm-dpc/COVID-19) | NUTS 0-3, Italy |
| **RKI** | [Robert Koch-Institut, Germany](https://npgeo-corona-npgeo-de.hub.arcgis.com/datasets/dd4580c810204019a7b8eb3e0b329dd6_0) | NUTS 0-3, Germany |

## Credits

This work is supported by NASA Health & Air Quality project `80NSSC18K0327`, under a COVID-19 supplement.

## Citation

To cite this dataset:

> Badr, H. S., B. F. Zaitchik, G. H. Kerr, J. M. Colston, P. Hinson, Y. Chen, N. H. Nguyen, M. Kosek, H. Du, E. Dong, and L. M. Gardner, **2020**: Unified COVID-19 Dataset. _GitHub_, `https://github.com/hsbadr/COVID-19`.
