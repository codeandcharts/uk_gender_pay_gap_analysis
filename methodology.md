# UK Gender Pay Gap Analysis: Methodology Document

## Project Overview

This project analyzes the UK gender pay gap from 2017-2025 using official government reporting data. The analysis examines trends over time, variations across different organizational characteristics (size, sector, region), and the relationship between different pay gap metrics. The goal is to identify structural patterns in pay inequality and develop targeted recommendations for accelerating progress toward equity.

## Dataset Description

### Data Source
- **Primary dataset**: UK Government Gender Pay Gap Service
- **Coverage**: 2017-2025 reporting years
- **Scope**: All UK employers with 250+ employees required to report
- **Records**: Approximately 80,000 employer reports across 9 reporting years

### Key Variables

The dataset contains the following primary variables:

#### Organizational Identifiers
- **EmployerId**: Unique identifier for each employer
- **EmployerName**: Name of the reporting organization
- **EmployerSize**: Categorical variable with 7 size bands (Less than 250, 250-499, 500-999, 1000-4999, 5000-19999, 20000+, Not Provided)
- **SectorType**: Industry sector classification 
- **CompanyNumber**: Companies House registration number
- **Region**: Geographic region (England, Scotland, Wales, Northern Ireland)

#### Pay Gap Metrics
- **DiffMeanHourlyPercent**: Mean gender pay gap in hourly pay
- **DiffMedianHourlyPercent**: Median gender pay gap in hourly pay
- **DiffMeanBonusPercent**: Mean gender pay gap in bonus pay
- **DiffMedianBonusPercent**: Median gender pay gap in bonus pay

#### Gender Distribution Variables
- **MaleBonusPercent**: Percentage of male employees receiving a bonus
- **FemaleBonusPercent**: Percentage of female employees receiving a bonus
- **MaleLowerQuartile**: Percentage of males in lowest pay quartile
- **FemaleLowerQuartile**: Percentage of females in lowest pay quartile
- **MaleLowerMiddleQuartile**: Percentage of males in lower-middle pay quartile
- **FemaleLowerMiddleQuartile**: Percentage of females in lower-middle pay quartile
- **MaleUpperMiddleQuartile**: Percentage of males in upper-middle pay quartile
- **FemaleUpperMiddleQuartile**: Percentage of females in upper-middle pay quartile
- **MaleTopQuartile**: Percentage of males in highest pay quartile
- **FemaleTopQuartile**: Percentage of females in highest pay quartile

#### Reporting Variables
- **SubmittedAfterDeadline**: Boolean indicating late reporting
- **ReportingYear**: Year of the report (2017-2025)
- **ReportingDate**: Date report was submitted

## Methodology

### Data Preparation

1. **Data Cleaning**:
   - Removed duplicate records based on EmployerId and ReportingYear
   - Addressed missing values through appropriate imputation techniques
   - Validated that quartile percentages summed to 100% within each gender
   - Checked for and addressed logical inconsistencies in the data

2. **Outlier Analysis**:
   - Identified extreme outliers in pay gap metrics through boxplot visualization
   - Applied the IQR method to detect statistical outliers
   - Created separate visualizations before and after outlier treatment to understand their impact
   - Preserved extreme values when they represented genuine cases rather than data errors

3. **Feature Engineering**:
   - Created a QuartileDifference variable (FemaleTopQuartile - FemaleLowerQuartile) to measure vertical segregation
   - Calculated year-over-year changes in key metrics
   - Developed composite metrics to measure overall organizational equity

### Exploratory Data Analysis

1. **Univariate Analysis**:
   - Distribution analysis of all pay gap metrics
   - Histograms and density plots for key variables
   - Summary statistics for central tendency and dispersion

2. **Bivariate Analysis**:
   - Correlation analysis between all numeric variables
   - Scatter plots examining relationships between different pay gap metrics
   - Cross-tabulations of categorical variables

3. **Time Series Analysis**:
   - Trend analysis of pay gap metrics over the 2017-2025 period
   - Identification of key turning points in the trend
   - Year-over-year change calculations

4. **Categorical Analysis**:
   - ANOVA to test for significant differences between organization sizes, sectors, and regions
   - Box plots and violin plots to visualize distribution differences
   - Bar charts showing aggregated metrics by categorical variables

### Statistical Methods

1. **Correlation Analysis**:
   - Calculated Pearson correlation coefficients between all numerical variables
   - Generated correlation matrix visualization to identify relationship patterns
   - Tested statistical significance of key correlations

2. **Comparative Statistics**:
   - T-tests comparing means across different groups (reporting timeliness, organization size)
   - Chi-square tests for categorical variable relationships
   - ANOVA tests for multi-group comparisons

3. **Regression Analysis**:
   - Multiple linear regression to identify predictors of hourly and bonus pay gaps
   - Time series regression to analyze and project trends
   - Controlled for relevant covariates to isolate key effects

### Visualization Approach

1. **Time Series Visualizations**:
   - Line charts with multiple series to compare different gap metrics over time
   - Area charts to show gender composition changes in quartiles
   - Trend lines with confidence intervals for projections

2. **Distribution Visualizations**:
   - Box plots showing distributions by employer size and region
   - Violin plots comparing distributions between groups
   - Histograms and kernel density plots for continuous variables

3. **Categorical Comparisons**:
   - Bar charts showing pay gaps by sector, size, and region
   - Heatmaps showing correlation patterns
   - Stacked bar charts showing gender composition

4. **Geographic Visualizations**:
   - Choropleth maps of regional pay gaps across the UK
   - Regional comparison charts

## Limitations and Considerations

1. **Self-Reported Data**:
   - The analysis relies on self-reported data from employers, which may contain reporting errors
   - Data quality improved over time as reporting standards matured

2. **Survivorship Bias**:
   - Only includes organizations that existed throughout the reporting period
   - Companies that went out of business or fell below the 250-employee threshold exit the dataset

3. **Simplification of Complex Phenomena**:
   - Pay gap metrics are high-level measures that may obscure nuanced causes
   - Limited controls for occupation, experience, or education differences

4. **Causality Constraints**:
   - The analysis identifies correlations and patterns but cannot definitively establish causality
   - Multiple interpretations of observed relationships may be valid

5. **COVID-19 Impact**:
   - The 2020-2021 data was affected by the COVID-19 pandemic, potentially distorting typical patterns
   - Some reporting requirements were modified during this period

## Software and Tools

- **Programming**: Python 3.11
- **Core Libraries**: pandas, numpy, scikit-learn
- **Visualization**: matplotlib, seaborn
- **Statistical Analysis**: scipy.stats
- **Data Processing**: Jupyter Notebooks
- **Version Control**: Git/GitHub

## Ethical Considerations

This analysis was conducted with attention to:
- Data privacy requirements
- Fair representation of findings
- Acknowledgment of limitations
- Avoidance of misleading visualizations
- Transparency in methodology