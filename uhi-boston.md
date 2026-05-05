# Urban Heat Island Equity Analysis - Boston, MA

## Study Area and Data
This study examines urban heat island patterns across Boston, Massachusetts and adjacent municipalities using census tracts as the unit of analysis. The aerial imagery used in the study was collected on July 30, 2025, which was selected based on minimal cloud cover and high air temperatures (~86°F), to provide reliable land surface temperature data and to capture peak urban heat island conditions.

Datasets: Landsat 9 (Collection 2 Level-2), 2020 Census Tracts (MassGIS), 2022 American Community Survey 5-year estimates; accessed via NHGIS (IPUMS).

### Land Surface Temperature (LST)
![LST Map](images/lst_map.png)
Land surface temperatures are highest in Roxbury, South Boston, Allston, Cambridge, Somerville, Everett, Medford, Chelsea, and East Boston. 

### Residual LST (Observed vs Expected)
![Residual Map](images/residual_map.png)

### Heat Vulnerability Index (HVI)
![HVI Map](images/hvi_map.png)

### Priority Heat Intervention Areas
![Priority Map](images/priority_map.png)

## Key Findings
- Built environment is the primary driver of urban heat
- Vegetation is strongly associated with lower surface temperatures
- Socially vulnerable populations are disproportionately exposed to high temperatures
- Priority heat intervention areas identified across Boston and adjacent municipalities

## Methods
- Landsat 9 used to derive LST, NDVI, and NDBI
- Demographic data agreggated to Census tract-level using zonal statistics
- Correlation and regression analysis
- Heat Vulnerability Index created by normalizing and averaging LST, percent minority, and poverty rate variables

## Full Report
[Download Full Report](./UHI_Analysis.pdf)
