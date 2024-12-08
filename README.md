# Analysis of the EJ Impacts of the 2021 Texas Winter Storm

Extreme weather events are becoming more frequent and intense due to climate change, causing significant disruptions to infrastructure and society. In February 2021, Texas experienced a severe power crisis caused by three successive winter storms (February 10–11, 13–17, and 15–20).

This project analyzes the impacts of the storms on power availability in the Houston metropolitan area by estimating the number of homes affected by power outages and assessing whether these impacts were disproportionately distributed.

## **Repository Structure**

- `analysis_files/`                # Folder containing analysis-related files
- `.DS_Store`                      # macOS system file (generally ignored by Git)
- `.gitignore`                     # Git ignore file to exclude unnecessary files
- `EJ Impacts of the 2021 Texas Winter Storm.Rproj`   # R project file for analysis
- `LICENSE`                        # License file for the project
- `README.md`                      # Project documentation
- `analysis.html`                  # Generated HTML report
- `analysis.qmd`                   # Quarto markdown file for analysis

  
## Data Overview:
#### **Night Lights**  
- **Purpose**: Analyze power outages in Texas during February 2021 using nightlight imagery.
- **Key Dates**:  
  - **2021-02-07**: Pre-outage reference.  
  - **2021-02-16**: Post-outage impact.  
- **Files**:  
  - `h08v05` and `h08v06` tiles for both dates:  
    - 2021-02-07: `VNP46A1.A2021038.*.tif`  
    - 2021-02-16: `VNP46A1.A2021047.*.tif`
- **Source**: [NASA’s Worldview and VIIRS data via LAADS DAAC](https://ladsweb.modaps.eosdis.nasa.gov/)  

#### **Roads** 
- **Purpose**: Exclude highways to minimize false positives in nightlight reduction analysis. 
- **File**: `gis_osm_roads_free_1.gpkg`  
- **Source**: [OpenStreetMap data (subset for Houston)](https://download.geofabrik.de/)

#### **Houses**  
- **Purpose**: Identify houses affected by the power outage.
- **File**: `gis_osm_buildings_a_free_1.gpkg`  
- **Source**: [OpenStreetMap data (subset for Houston)](https://download.geofabrik.de/)

#### **Socioeconomic Data** 
- **Purpose**: Link ACS 2019 census tract attributes (e.g., socioeconomic data) to geographic features in Houston.
- **File**: `ACS_2019_5YR_TRACT_48.gdb` (ArcGIS geodatabase).  
- **Source**: [U.S. Census Bureau’s American Community Survey](https://www.census.gov/programs-surveys/acs)

## Author
Sanjay Poudel


