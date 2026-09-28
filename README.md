# London Smart Meter Consumption Analysis

MSc Data Analytics dissertation project at Queen Mary University of London.

This project investigates whether clustering of household electricity consumption
profiles reveals genuinely distinct consumer groups or primarily reflects differences
in overall energy consumption.

The analysis uses the London Smart Meters dataset and examines 2,138 households
represented by half-hourly electricity consumption profiles.

## Key Questions

- What does standard load-profile clustering actually capture?
- Are the identified clusters evidence of distinct consumer groups?
- How does data representation affect clustering results?
- What are the implications for electricity network planning and demand-side management?

## Methods

- Data cleaning and preprocessing
- Exploratory Data Analysis (EDA)
- Time-series load profile analysis
- K-Means clustering
- K-Medoids clustering
- Hierarchical clustering
- Gaussian Mixture Models
- DBSCAN
- PCA
- Euclidean distance and Dynamic Time Warping (DTW)
- Silhouette Score
- Davies-Bouldin Index
- Calinski-Harabasz Index
- Gap Statistic
- Bootstrap stability analysis
- Consensus clustering
- Statistical hypothesis testing
- Synthetic-data validation

## Key Findings

- Clustering of raw electricity profiles was primarily driven by total daily
  electricity consumption rather than differences in profile shape.

- The K-Means partition agreed with a simple consumption-based segmentation for
  98.5% of households (Adjusted Rand Index = 0.962).

- The first principal component explained 81.1% of the variance and was almost
  perfectly correlated with daily electricity consumption.

- Statistical tests did not provide evidence of naturally distinct consumer groups.

- Synthetic datasets without inherent cluster structure produced similar clustering
  behaviour, showing that stable clusters do not necessarily imply real population
  segments.

- Using averaged cluster profiles can distort estimates of electricity network
  capacity.

- Simulated demand shifting produced a maximum system-wide peak reduction of
  approximately 0.7%.

## Dataset

London Smart Meters dataset from the Low Carbon London project.

The original dataset contains half-hourly electricity consumption readings from
5,567 London households. After data-quality filtering and outlier removal, the final
analysis used 2,138 households.

## Technologies

Python · Pandas · NumPy · Scikit-learn · SciPy · Matplotlib · Jupyter Notebook

## Repository Structure

```text
├── notebooks/
│   └── load_profile_analysis.ipynb
├── figures/
├── dissertation.pdf
├── requirements.txt
└── README.md
