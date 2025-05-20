# Cleaning the shorebird survey data

## The original data set

ARCTIC SHOREBIRD DEMOGRAPHICS NETWORK [https://doi.org/10.18739/A2222R68W](https://doi.org/10.18739/A2222R68W)

Data set hosted by the [NSF Arctic Data Center](https://arcticdata.io) data repository 

Field data on shorebird ecology and environmental conditions were collected from 1993-2014 at 16 field sites in Alaska, Canada, and Russia.

![Shorebird, copyright NYT](https://static01.nyt.com/images/2017/09/10/nyregion/10NATURE1/10NATURE1-superJumbo.jpg?quality=75&auto=webp)

Data were not collected every year at all sites. Studies of the population ecology of these birds included nest-monitoring to determine the timing of reproduction and reproductive success; live capture of birds to collect blood samples, feathers, and fecal samples for investigations of population structure and pathogens; banding of birds to determine annual survival rates; resighting of color-banded birds to determine space use and site fidelity; and use of light-sensitive geolocators to investigate migratory movements. 

Data on climatic conditions, prey abundance, and predators were also collected. Environmental data included weather stations that recorded daily climatic conditions, surveys of seasonal snowmelt, weekly sampling of terrestrial and aquatic invertebrates that are prey of shorebirds, live trapping of small mammals (alternate prey for shorebird predators), and daily counts of potential predators (jaegers, falcons, foxes). Detailed field methods for each year are available in the `ASDN_protocol_201X.pdf` files. All research was conducted under permits from relevant federal, state, and university authorities.

See `01_ASDN_Readme.txt` provided in the [course data repository](https://github.com/UCSB-Library-Research-Data-Services/bren-meds213-spring-2024-class-data) for full metadata information about this raw data set.

## Purpose

The purpose of this repository is to clean the snow survey data included in this dataset. 

## Data & File Overview

#### File List:

```
.
├── README.md
├── .gitignore
├── eds213_data_cleaning_assign_marina-kochuten.qmd   # File for data cleaning
└── data/
    ├── processed/                                    # Cleaned data/
    │   ├── all_cover_fixed_marina_kochuten.csv       # Fully cleaned snow survey data
    │   └── snow_cover.csv                            # Partially cleaned
    └── raw/                                          # Original data/
        ├── 01_ASDN_Readme.txt                        # Original metadata
        ├── ASDN_Daily_Species.csv                    # Species survey data
        └── ASDN_Snow_Survey                          # Snow cover survey data
```


#### Additional related data collected that was not included in the current data package:

There are many other related tables that are not included in this repository including:

- Bird_captures
- Bird_eggs
- Bird_nests
- Bird_resights
- Bird_sexes
- Camp_info
- Camp_staff
- Daily_pred_lemm
- Daily_species_effort
- Geodata
- Invert_biomass
- Lemming_counts
- Lemming_nests
- Lemming_trap
- Pred_nests
- Pred_point_counts
- Study_Plot	(KMZ file)
- Surface_water
- Weather_HOBO
- Weather_precip_manual
- Weather_snow_manual

Each data file is available on the ASDN page at the [NSF Arctic Data Center](https://arcticdata.io) and is a .csv file with prefix "ASDN_"

#### Other versions of this dataset:

The datasets used in this repository are from the course EDS 213 - Databases and Data Management. Data used in the course are cleaned-up subsets of the full dataset. Data was subset to keep the size and complexity manageable for pedagogical purposes.


## Info for cleaned snow cover data

**File:** data/processed/all_cover_fixed_YOURNAME.csv : 

**Number of variables:** 11

**Number of cases/rows:** 42,830

**Variable List:**

| Variable name | Description                                                                                                                                                           | Unit(s) / Value type |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| Site          | Four-letter code of site at which data were collected                                                                                                                 | string               |
| Year          | Year in which data were collected                                                                                                                                     | integer              |
| Date          | Date on which data were collected                                                                                                                                     | date                 |
| Plot          | Name of study plot on which survey was conducted                                                                                                                      | string               |
| Location      | Name of dedicated snow-survey location, if applicable                                                                                                                 | string               |
| Snow_cover    | Percent cover of snow, including slush                                                                                                                                | integer              |
| Water_cover   | Percent cover of water                                                                                                                                                | integer              |
| Land_cover    | Percent cover of exposed land                                                                                                                                         | integer              |
| Total_cover   | Sum of previous three _cover variables. Values either 100 or NA.  If NA, _cover variables do not add to 100, suggesting instances of incomplete land cover surveying. | integer              |
| Observer      | Person who conducted the survey                                                                                                                                       | string               |
| Notes         | Any relevant comments on the survey                                                                                                                                   | string               |

**Missing data codes:**
   
Missing data encoded as NA.

Note that in Total_cover column, NA values indicate that _cover columns do not sum to 100. 


SHARING/ACCESS INFORMATION

1. Licenses/restrictions placed on the data:

2. Links to publications that cite or use the data:

3. Links to other publicly accessible locations of the data:

4. Links/relationships to ancillary data sets: <any supplementary data sources 
that support analysis or classification of the datasets, eg., plant taxonomy table.)>

5. Was data derived from another source? If yes, list source(s): <list citations 
to original sources>

6. Recommended citation for the project:
