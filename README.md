# Global-Pulse-Inequality-Emissions-Atlas
The Global-Pulse Atlas is an interactive analytical suite designed to help stakeholders visualize the dual-crisis of socio-economic inequality and environmental degradation. By layering GINI indices over CO2 emissions and population metrics, the project identifies regions where high inequality and high emissions create unique policy challenges.

## Technical Depth & Analytical Thinking
### 1. Complex Data Engineering & Normalization
Real-world socio-economic data is often fragmented. This project demonstrates high-level data wrangling skills:

**Temporal Imputation:** Implemented Forward-Filling (FFill) and Back-Filling (BFill) strategies to handle significant gaps in the GINI index (1990–2020), ensuring a continuous temporal narrative without compromising statistical integrity.

**Multi-Source Merging:** Synthesized data from the World Bank (GINI), Our World in Data (CO2 & Population), and Kaggle (Geospatial coordinates).

**Standardization Pipeline:** Engineered a normalization layer to resolve name discrepancies between TopoJSON map files and CSV datasets (e.g., mapping "United States" to "United States of America" for seamless choropleth rendering).

### 2. Advanced Geospatial Visualization (Altair)
I leveraged the Altair declarative visualization library to build a multi-layered, interactive experience:

**Layered Visual Hierarchy:** Designed a 5-layer map stack:

**Ocean Sphere:** Pale blue base for geographic context.

**Graticules:**  Lat/Lon gridlines for technical precision.

**Population Choropleth:** A log-scaled background map depicting population density using a brownbluegreen scheme.

**Static Labels:** High-contrast continent markers for rapid orientation.

**Dynamic Bubbles:** A temporal layer where Bubble Size = CO2 Emissions and Bubble Color = GINI Index (Magma Scheme).

**Interactive Temporal Scrubbing:** Integrated an Altair binding_range slider, allowing users to move through time from 1990 to 2020 and watch the evolution of global inequality in real-time.

## Business & ESG Insights
**ESG Reporting:** This tool serves as a prototype for Corporate Social Responsibility (CSR) and Environmental, Social, and Governance (ESG) dashboards, helping firms identify risk zones where social disparity meets high environmental impact.

**Resource Allocation:** By identifying "hotspots" (high GINI + high CO2), policy-makers can better direct sustainability grants and social welfare programs.

**Strategic Storytelling:** The use of interactive visualization reduces cognitive load for non-technical executives, transforming complex statistical correlations into intuitive geographic insights.

## Technical Stack
Visualization: Altair 5 (Selection points, Layering, Geospatial projections).

Data Analysis: Pandas (Multi-index merging, GroupBy transformations).

Geospatial: TopoJSON, EqualEarth Projections.

Environment: Python 3.x, KaggleHub.
