---
title: Urban Heat Island Equity Analysis - Boston Metropolitan Area
---

<style>
.main-content {
  max-width: 1100px;
}

.figure {
  text-align: center;
  margin: 3rem 0;
}

.figure img {
  width: 100%;
  max-width: 1000px;
  height: auto;
  border-radius: 10px;
  border: 1px solid #d1d5db;
  box-shadow: 0 4px 14px rgba(0,0,0,0.08);
}

.figure.chart img {
  max-width: 775px;
}

.caption {
  text-align: left;
  font-size: 1rem;
  color: #444;
  margin: 0.75rem auto 0 auto;
  max-width: 1000px;
  line-height: 1.6;
}

.figure.chart .caption {
  max-width: 775px;
}

.section-divider {
  margin: 4rem 0 2rem 0;
  border-top: 1px solid #e5e7eb;
}

.quickfacts {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 1rem;
  margin: 2rem 0;
}

.factbox {
  border: 1px solid #d1d5db;
  border-radius: 10px;
  padding: 1rem;
  background-color: #fafafa;
}

.factbox strong {
  display: block;
  margin-bottom: 0.5rem;
}

p, li {
  line-height: 1.7;
}

.footer-col-1 {
  display: none;
}

.footer-col-2 {
  display: none;
}

.footer-col-3 {
  width: 100%;
}
</style>

This study examines urban heat island patterns across Boston, Massachusetts and adjacent municipalities using census tracts as the unit of analysis. The satellite imagery used in the study was collected on July 30, 2025, which was selected because of minimal cloud cover and high air temperatures (~86°F) to provide reliable land surface temperature (LST) data and to capture peak urban heat island conditions.

Datasets: Landsat 9 (Collection 2 Level-2), 2020 Census Tracts (MassGIS), 2022 American Community Survey (ACS) 5-year estimates; accessed via NHGIS (IPUMS).

<div class="section-divider"></div>

## Workflow

- Landsat 9 used to derive LST, vegetation (NDVI), and built-up (NDBI) indices. Data were aggregated to the census tract level using zonal statistics.
- Percent minority and poverty rate were derived from ACS data and joined to census tract geometries.
- Correlation and regression analysis were conducted on LST and independent variables: NDVI, NDBI, median income, percent minority, and poverty rate.
- Residual LST was calculated as the difference between observed and predicted LST based on the regression model between LST and NDVI.
- Heat Vulnerability Index (HVI) was created by normalizing and averaging LST, percent minority, and poverty rate variables.
- Urban heat intervention priority areas were identified by summing binary values for the top 10% highest LST, 25% highest NDBI, and 20% highest HVI tracts.

<div class="section-divider"></div>

## Visualizations

<div class="figure">
  <img src="images/lst_map.png" alt="Land surface temperature map of Boston census tracts">
  <p class="caption"><strong>Figure 1.</strong> LST is highest in Roxbury, South Boston, Allston, Cambridge, Somerville, Everett, Medford, Chelsea, and East Boston.</p>
</div>

<div class="figure chart">
  <img src="images/ndvi_lst_scatterplot.png" alt="Scatterplot showing the relationship between NDVI and land surface temperature">
  <p class="caption"><strong>Figure 2.</strong> The regression model shows an inverse relationship between vegetation cover and LST. A 0.1 increase in NDVI corresponds to an approximate 3.4°C decrease in LST.</p>
</div>

<div class="figure">
  <img src="images/residual_map.png" alt="Residual land surface temperature map of Boston census tracts">
  <p class="caption"><strong>Figure 3.</strong> Several neighborhoods in northern Boston and parts of Roxbury, Dorchester, and South Boston exhibit positive residuals, indicating factors beyond vegetation, such as building density and impervious surfaces, are contributing to higher LST. Coastal areas exhibit negative residuals likely due to cooling effects of the Atlantic Ocean and the Charles River.</p>
</div>

<div class="figure">
  <img src="images/hvi_map.png" alt="Heat Vulnerability Index map of Boston census tracts">
  <p class="caption"><strong>Figure 4.</strong> Census tracts in Roxbury, the South End, South Boston, Dorchester, Allston, Medford, Everett, Revere, and Chelsea contain the highest HVI values. These are locations where both environmental and social vulnerability risk factors are present.</p>
</div>

<div class="figure chart">
  <img src="images/hvi_barchart.png" alt="Average land surface temperature by Heat Vulnerability Index group">
  <p class="caption"><strong>Figure 5.</strong> Census tracts in the top 20% of the HVI experience average LST approximately 2.6°C higher than the rest of the study area.</p>
</div>

<div class="figure chart">
  <img src="images/pctmin_boxplot.png" alt="Distribution of land surface temperature by minority population group">
  <p class="caption"><strong>Figure 6.</strong> Census tracts with a lower percentage of minority population exhibit a wider LST range, possibly reflecting the presence of both dense urban areas and more vegetated neighborhoods.</p>
</div>

<div class="figure">
  <img src="images/priority_map.png" alt="Urban heat intervention priority areas map of Boston">
  <p class="caption"><strong>Figure 7.</strong> Urban heat intervention priority areas were identified by combining binary values for the top 10% highest LST, 25% highest NDBI, and 20% highest HVI tracts. A priority score was calculated as the sum of these values. The highest priority areas are in South Boston, the South End, Roxbury, Allston, Chelsea, Everett, Medford, and East Boston.</p>
</div>

<div class="section-divider"></div>

## Key Findings

- Built environment is the primary driver of urban heat, and proximity to bodies of water has a significant cooling effect.
- Vegetation is strongly associated with lower LST, while percent minority population and poverty rate show weaker but still meaningful spatial relationships with higher LST.
- Socially vulnerable populations are located disproportionately in areas with higher exposure to extreme heat.
- Urban heat intervention priority areas were identified in South Boston, the South End, Roxbury, Allston, Chelsea, Everett, Medford, and East Boston. These areas would benefit from targeted urban cooling strategies such as green infrastructure, reflective pavements or roofing, tree planting, and water features.

<div class="section-divider"></div>

## Full Report

[Download Full Report](./UHI_Analysis.pdf)
