# NYC Building Energy Efficiency Analysis

## This project analyzes energy and water consumption data from New York City buildings (Local Law 84, 2016) to identify patterns and predict Energy Star scores. The analysis focuses on preprocessing, feature engineering, and building a baseline model for energy efficiency assessment.

### Data Source
 -  Dataset: Energy and Water Data Disclosure for Local Law 84 2017 (Calendar Year 2016)
 -  Source: NYC Open Data
 -  Records: Building-level energy and water consumption metrics
 -  Key Metric: ENERGY STAR Score (renamed to score)

### Features & Preprocessing
#### 1. Data Cleaning
  - Replaced "Not Available" and "Not Avai" with NaN
  - Converted energy/water-related columns to float: Square footage (`ft²`), Energy usage (`kBtu`, `kWh`, `therms`), Water consumption (`gal`), Greenhouse gas emissions (`Metric Tons CO2e`), ENERGY STAR Score


#### 2. Missing Value Analysis
  - Identified columns with >50% missing values (removed)
  - Generated missing value statistics report

#### 3. Feature Engineering
  - Numerical Features: Original numeric columns
  - Added transformations:
    - Square root transformation
    - Logarithmic transformation
  - Categorical Features:
    - `Borough` (one-hot encoded)
    - `Largest Property Use Type` (one-hot encoded)
    - Filtered to include only property types with >100 occurrences

#### 4. Correlation Analysis
  - Computed correlations with Energy Star Score
  - Removed highly correlated features
  - Created visualization pairs for key metrics:
    - Site EUI
    - Weather Normalized Source EUI
    - Log-transformed GHG Emissions


### Exploratory Data Analysis

#### Correlation Matrix & Pair Plots
  - Upper triangle: Scatter plots
  - Diagonal: Histograms
  - Lower triangle: Correlation coefficients + KDE plots


#### Key Visualized Metrics:
  - `score`: ENERGY STAR Score
  - `Site EUI (kBtu/ft²)`: Site Energy Use Intensity
  - `Weather Normalized Source EUI (kBtu/ft²)`: Weather-adjusted energy use
  - `log_Total GHG Emissions`: Log-transformed greenhouse gas emissions


### Visualization:
<img width="748" height="338" alt="image" src="https://github.com/user-attachments/assets/248cfbc1-e947-4800-b136-b7ad83325054" />

<img width="744" height="375" alt="image" src="https://github.com/user-attachments/assets/e31f3db5-85b5-4dee-8104-a9e7420f4b64" />


