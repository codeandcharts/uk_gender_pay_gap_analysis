# UK Gender Pay Gap Analysis

![Project Banner](./images/project_banner.png)

## Overview

This repository contains a comprehensive analysis of the UK gender pay gap from 2017 to 2025, using official government reporting data. The project explores trends over time, variations across different organizational characteristics, and relationships between different pay gap metrics to identify structural patterns in pay inequality and develop targeted recommendations.

## Key Findings

- The overall gender pay gap has decreased from 15% in 2020 to 12.1% in 2025
- Bonus pay gaps (28-34%) are more than double hourly pay gaps (12-14.7%)
- Mid-sized organizations (5,000-19,999 employees) show the highest gaps (14.2%)
- England shows higher gaps (12.5%) than other UK regions, with Northern Ireland lowest (7.8%)
- Female representation in top pay quartiles has improved to approximately 40% by 2024

## Repository Structure

```
uk-gender-pay-gap-analysis/
│
├── data/                      # Data directory
│   ├── raw/                   # Raw data files
│   ├── processed/             # Cleaned and processed data
│   └── external/              # External reference data
│
├── notebooks/                 # Jupyter notebooks
│   ├── 01_data_cleaning.ipynb         # Data preprocessing & cleaning
│   ├── 02_exploratory_analysis.ipynb  # EDA & visualization
│   ├── 03_statistical_analysis.ipynb  # Statistical testing
│   ├── 04_time_series_analysis.ipynb  # Temporal pattern analysis
│   └── 05_regional_analysis.ipynb     # Geographic analysis
│
├── src/                       # Source code
│   ├── data/                  # Data processing scripts
│   ├── features/              # Feature engineering
│   ├── visualization/         # Visualization functions
│   └── models/                # Statistical models
│
├── reports/                   # Generated analysis reports
│   ├── figures/               # Generated graphics and figures
│   └── UK_Gender_Pay_Gap_Analysis.pdf  # Final report
│
├── requirements.txt           # Project dependencies
├── environment.yml            # Conda environment file
├── methodology.md             # Detailed methodology documentation
└── README.md                  # This file
```

## Dataset Description

The dataset includes approximately 80,000 employer reports across nine reporting years (2017-2025). All UK employers with 250+ employees are required to report their gender pay gap data annually.

### Key Variables

- **Pay Gap Metrics**: Mean/median hourly and bonus pay gaps
- **Gender Distribution**: Percentage of employees by gender across pay quartiles
- **Organizational Details**: Employer size, sector, region
- **Reporting Information**: Submission date, compliance status

## Installation and Usage

### Prerequisites
- Python 3.11+
- pip or conda for package management

### Setup
1. Clone this repository:
   ```
   git clone https://github.com/yourusername/uk-gender-pay-gap-analysis.git
   cd uk-gender-pay-gap-analysis
   ```

2. Create and activate environment:
   ```
   # Using pip
   python -m venv .venv
   source .venv/bin/activate  # On Windows: .venv\Scripts\activate
   pip install -r requirements.txt
   
   # OR using conda
   conda env create -f environment.yml
   conda activate uk-gender-pay-gap
   ```

3. Run Jupyter notebooks:
   ```
   jupyter lab
   ```

### Reproducing the Analysis

The analysis can be reproduced by running the notebooks in numerical order:
1. Data cleaning and preprocessing
2. Exploratory data analysis
3. Statistical testing and modeling
4. Time series analysis
5. Regional analysis

## Visualization Gallery

The project includes various visualizations that reveal key patterns:

- Time series plots showing pay gap trends from 2017-2025
- Box plots displaying distributions by employer size and region
- Bar charts comparing pay gaps across sectors
- Choropleth maps of regional variations
- Distribution plots showing hourly vs. bonus pay gaps

## Main Recommendations

Based on the analysis, the following recommendations are proposed:

1. **Transform Bonus Systems**: Implement transparent criteria for bonus allocation
2. **Target Mid-Sized Organizations**: Develop specialized programs for organizations with 5,000-19,999 employees
3. **Adapt Regional Best Practices**: Study and implement policies from lower-gap regions across the UK
4. **Support Vertical Mobility**: Create programs to advance women from middle to upper pay quartiles
5. **Develop Sector-Specific Strategies**: Create tailored approaches for high-gap sectors

## Methodology

A detailed methodology document is available in [methodology.md](methodology.md), covering:
- Data preparation and cleaning procedures
- Statistical methods
- Visualization approaches
- Limitations and considerations

## Dependencies

- **Data Processing**: pandas, numpy
- **Visualization**: matplotlib, seaborn
- **Statistical Analysis**: scipy, statsmodels
- **Machine Learning**: scikit-learn

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- UK Government Gender Pay Gap Service for providing the data
- All employers who submitted comprehensive reports
- Open source Python community for the tools used in this analysis

## Contact

For questions or feedback, please contact:
- Your Name - [your.email@example.com](mailto:your.email@example.com)
- Project Link: [https://github.com/yourusername/uk-gender-pay-gap-analysis](https://github.com/yourusername/uk-gender-pay-gap-analysis)