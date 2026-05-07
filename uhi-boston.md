# Urban Heat Island Equity Analysis - Boston, MA

This study examines urban heat island patterns across Boston, Massachusetts and adjacent municipalities using census tracts as the unit of analysis. The satellite imagery used in the study was collected on July 30, 2025, which was selected because of minimal cloud cover and high air temperatures (~86°F) to provide reliable land surface temperature data and to capture peak urban heat island conditions.

Datasets: Landsat 9 (Collection 2 Level-2), 2020 Census Tracts (MassGIS), 2022 American Community Survey 5-year estimates; accessed via NHGIS (IPUMS).

## Workflow
- Landsat 9 used to derive LST, NDVI, and NDBI.
- Demographic data agreggated to Census tract-level using zonal statistics.
- Correlation and regression analysis on LST vs independent variables (NDVI, NDBI, median income, percent minority, poverty rate).
- Residual LST was calculated as the difference between observed and predicted LST based on the regression model between LST and NDVI.
- Heat Vulnerability Index created by normalizing and averaging LST, percent minority, and poverty rate variables.
- Urban heat intervention priority areas were identified by summing binary values for the top 10% highest LST, 25% highest NDBI, and 20% highest HVI tracts.

## Visualizations
![LST Map](images/lst_map.png)
Figure 1. Land surface temperatures are highest in Roxbury, South Boston, Allston, Cambridge, Somerville, Everett, Medford, Chelsea, and East Boston. The regression model (y=-34.2x+46.8) indicated an inverse relationship between NDVI and land surface temperature, and was used to create the residual LST map. 

![Residual Map](images/residual_map.png)
Figure 2. Several neighborhoods in northern Boston and parts of Roxbury, Dorchester, and South Boston exhibit positive residuals, indicating factors beyond vegetation, such as building density and impervious surfaces, are contributing to higher temperatures. Coastal areas exhibit negative residuals likely due to cooling effects of the Atlantic Ocean and the Charles River.

![HVI Map](images/hvi_map.png)
Figure 3. Census tracts in Roxbury, the South End, South Boston, Dorchester, Allston, Medford, Everett, Revere, and Chelsea contain the highest HVI values. These are locations where both environmental (LST) and social (percent minority and poverty rate) risk factors are present.

![LST vs HVI](images/hvi_barchart.png)
Figure 4. Census tracts in the top 20% of the HVI experience, on average, land surface temperatures 2.6°C higher than the rest of the study area.

![LST vs Pct Min](images/pctmin_boxplot.png)
Figure 5. There is a wider temperature range observed in tracts with a lower percentage of minority population, possibly reflecting the presence of both dense urban areas and neighborhoods with more vegetation.

![Priority Map](images/priority_map.png)
Figure 6. Urban heat intervention priority areas were identified by combining binary values for the top 10% highest LST, 25% highest NDBI, and 20% highest HVI tracts. A priority score was calculated as the sum of these values. The highest priority areas are in South Boston, the South End, Roxbury, Allston, Chelsea, Everett, Medford, and East Boston.

## Key Findings
- Built environment is the primary driver of urban heat and proximity to bodies of water has a significant cooling effect.
- Vegetation is strongly associated with lower surface temperatures, while percent minority population and poverty rate show weaker but still meaningful spatial relationships with higher LST.
- Socially vulnerable populations are located disproportionately in areas with higher exposure to extreme heat.
- Priority heat intervention areas identified in South Boston, the South End, Roxbury, Allston, Chelsea, Everett, Medford, and East Boston. These areas would benefit from targeted urban cooling strategies such as green infrastructure, reflective pavements or roofing, tree planting, and water features. 

## Full Report
[Download Full Report](./UHI_Analysis.pdf)
