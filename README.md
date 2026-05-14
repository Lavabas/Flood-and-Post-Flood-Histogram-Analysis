<img width="1105" height="393" alt="image" src="https://github.com/user-attachments/assets/a66a6e25-1b24-42ea-9f51-3ec721729a63" /># Flood-and-Post-Flood-Histogram-Analysis
## Overview

Floods are among the most destructive natural hazards in Sri Lanka, frequently causing damage to infrastructure, agriculture, ecosystems, and human settlements. Rapid identification of flood-affected areas is essential for disaster response, environmental monitoring, and risk assessment. Remote sensing provides an effective approach for monitoring floods over large regions where field observations may be limited.

This project demonstrates a flood detection and histogram-based flood analysis workflow using Landsat 8 surface reflectance imagery, Google Earth Engine (GEE), Xee, and Xarray. The study focuses on the severe May 2017 flood event in the Kalutara region of southwestern Sri Lanka, one of the most heavily affected areas during the disaster.

The workflow applies the Normalized Difference Water Index (NDWI) to compare pre-flood and flood-period surface water conditions. Spatial visualization and histogram analysis are used to evaluate how surface water distribution changed during the flood event.

The project highlights how open Earth Observation (EO) datasets and cloud-based geospatial processing tools can support flood monitoring and environmental analysis using Python-based workflows.

## Study Area
- The selected Region of Interest (ROI) covers part of the Kalutara District in southwestern Sri Lanka.
- This region experienced severe flooding during May 2017 due to intense monsoonal rainfall associated with a low-pressure system and the onset of the southwest monsoon.

## Objectives
1. Detect flood-induced surface water expansion
2. Compare pre-flood and flood-period water conditions
3. Analyze NDWI distribution changes using histograms
4. Visualize flood impacts spatially
5. Demonstrate a Python-based flood analysis workflow using GEE and Xarray

## Datasets Used
1. Landsat 8 Collection 2 Level 2

- Dataset: LANDSAT/LC08/C02/T1_L2

- Used for:
  - Surface reflectance retrieval
  - NDWI calculation
  - Flood mapping

- Spatial Resolution: 30 meters

- Temporal Coverage: January 2017 – June 2017

## Tools and Libraries
1. Google Earth Engine (GEE)
2. geemap
3. xarray
4. xee
5. matplotlib
6. shapely
7. NumPy
8. Python

<img width="1105" height="393" alt="image" src="https://github.com/user-attachments/assets/4c6ca145-87d0-43c6-a03b-10f0b3739e19" />

## Results Interpretation

1. The results clearly demonstrate flood-induced surface water expansion across the Kalutara region during the May 2017 flood event.
2. The pre-flood NDWI map represents baseline hydrological conditions before the disaster. Water bodies such as rivers, canals, wetlands, and coastal zones are visible with relatively moderate NDWI values.
3. In contrast, the flood-period NDWI map shows noticeably larger regions with higher NDWI values, particularly around river networks, floodplains, and low-lying areas. These expanded high-NDWI zones indicate temporary inundation and floodwater accumulation caused by the extreme rainfall event.
4. Several coastal and inland areas exhibit intensified blue tones during the flood period, reflecting increased surface water coverage.
5. The histogram comparison between pre-flood and flood conditions further confirms the flood signal.

## Key observations include:
- The flood histogram shifts toward higher NDWI values.
- Flood-period images contain a larger proportion of pixels with positive NDWI values.
- Increased positive NDWI values indicate expanded water-covered surfaces.
- The overlap between histograms suggests that some portions of the landscape remained unchanged during flooding.
- The histogram-based approach effectively captures overall hydrological changes at the regional scale.

## Overall Interpretation
- When interpreted together, the NDWI maps and histogram distributions demonstrate that the flood event significantly altered the surface water dynamics of the region. The workflow successfully identified inundated zones and quantified changes in water-related spectral characteristics during the disaster period. Overall, the analysis demonstrates the usefulness of satellite-derived water indices and cloud-based geospatial processing for flood detection and environmental monitoring.

## Limitations
1. Cloud Contamination
- Although QA masking was applied, residual cloud and cloud-shadow artifacts remain in some images.

2. Optical Sensor Limitations
- Landsat optical imagery cannot penetrate clouds, which limits visibility during severe storm conditions.

3. Mixed Pixels
- Urban surfaces, wetlands, vegetation, and coastal water can produce mixed spectral responses that affect NDWI interpretation.

4. Temporal Resolution
- Landsat revisit intervals may not perfectly capture peak flood timing.

5. Coastal Influence
- Parts of the ROI include ocean and estuarine environments that naturally exhibit high NDWI values.

6. Sentinel-1 SAR Analysis Challenges
- A Sentinel-1 SAR-based flood workflow was also explored because SAR imagery can penetrate clouds and is generally considered more suitable for flood monitoring during storm events. However, the generated outputs were not fully satisfactory for this specific study area and workflow configuration. Possible reasons include speckle noise, backscatter variability over urban and vegetated surfaces, limited image availability during the exact flood peak, and difficulties in distinguishing floodwater from permanently low-backscatter surfaces. Consequently, the final analysis relied primarily on the Landsat-based NDWI approach for clearer visual interpretation and histogram comparison.


## Applications
1. Flood monitoring
2. Disaster management
3. Hydrological analysis
4. Surface water assessment
5. Environmental monitoring
6. GIS and Remote Sensing education

