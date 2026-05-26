# Strategic Humanitarian Aid Allocation

An end-to-end data science pipeline utilizing dimensionality reduction and clustering algorithms to analyze socio-economic indicators and identify countries in urgent need of humanitarian aid.

## Overview
This project explores global socio-economic and health disparities using a dataset of 167 countries. By applying standard scaling, Principal Component Analysis (PCA), and K-Means clustering, the global landscape is segmented into distinct development tiers (Developed, Developing, and Underdeveloped). The primary objective is to objectively identify the most vulnerable nations to optimize the allocation of financial, medical, and infrastructural relief.

## Project Structure
- `Strategic Humanitarian Aid Allocation.ipynb`: Jupyter notebook containing the full data pipeline, from preprocessing to cluster visualization.
- `Country-data.csv`: The primary dataset used for analysis, featuring metrics like child mortality, GDP per capita, and life expectancy.
- `Report.pdf`: The final academic summary detailing the methodology, visualizations, and strategic recommendations.

## Key Phases
1. **Data Preprocessing & PCA:** Applied Z-score normalization to ensure equal weighting across disparate metrics. Executed Principal Component Analysis (PCA) to eliminate multicollinearity, retaining 4 components that capture ~87.2% of the cumulative variance.
2. **Outlier Treatment:** Implemented Winsorization (capping at the 1st and 99th percentiles) directly on the PCA components to stabilize cluster centroids without dropping critical real-world extreme values.
3. **Clustering Analysis:** Utilized the Elbow Method and Silhouette Analysis to evaluate and optimize the **K-Means** algorithm, determining $K=3$ as the ideal mathematical and real-world segmentation.
4. **Strategic Prioritization:** Extracted the "Crisis/Aid" cluster and sorted the nations by lowest GDP per capita and highest child mortality to generate an actionable top-priority aid list.

## Key Technologies
- **Python:** Primary programming language for data manipulation.
- **Scikit-Learn:** Feature scaling (StandardScaler), dimensionality reduction (PCA), and unsupervised learning (K-Means).
- **Pandas & NumPy:** Data wrangling and numerical operations.
- **Seaborn & Matplotlib:** Statistical data visualization and scatter plots.
- **LaTeX:** Academic report typesetting.

## Metrics & Findings
| Metric / Finding | Value |
| :--- | :--- |
| **Optimal Clusters (K)** | 3 |
| **Crisis Cluster Avg. GDPP** | $1,767 |
| **Crisis Cluster Avg. Child Mort.** | 95.11 |
| **Top 5 Priority Nations** | Burundi, Liberia, Congo (Dem. Rep.), Niger, Sierra Leone |

## Author
**Sepehr Barekati**
