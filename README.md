# Venture Analytics

Analysis of Y Combinator companies with a focus on health and biotech investments over time.

## Overview

This repository contains data analysis and visualizations examining Y Combinator's investment patterns in health and biotech startups from 2005 to 2025. The analysis explores trends, geographic distribution, and the evolution of YC's focus on health-related companies.

## Data Source

The YC company data was scraped using [yc-scraper](https://github.com/corralm/yc-scraper).

## Repository Structure

```
venture-analytics/
├── data/
│   └── yc-data-2025.jl          # Raw YC company data (JSONL format)
├── notebooks/
│   ├── yc-analytics.ipynb       # Main analysis notebook
│   ├── yc_health_tags.txt       # List of health/biotech-related tags
│   └── yc_unique_tags.txt       # All unique tags in the dataset
└── README.md
```

## Key Files

### Notebooks

- **`yc-analytics.ipynb`**: Main Jupyter notebook containing:
  - Data preprocessing and cleaning
  - Tag normalization (lowercase, trimming)
  - Health company identification and filtering
  - Temporal analysis of YC's health/biotech investments
  - Geographic distribution analysis
  - Interactive visualizations using Plotly

### Data Files

- **`yc_health_tags.txt`**: Curated list of 45 health and biotech-related tags used to identify companies in the healthcare space, including:
  - Healthcare (healthcare, health-tech, digital-health)
  - Biotech (biotech, synthetic-biology, genomics)
  - Medical devices and diagnostics
  - Mental health and telehealth
  - Drug discovery and therapeutics

- **`yc_unique_tags.txt`**: Complete list of all 330+ unique tags found across all YC companies in the dataset

## Requirements

```
python>=3.8
pandas
plotly
jupyter
```

## Usage

1. Clone the repository
2. Install dependencies: `pip install pandas plotly jupyter`
3. Open and run `notebooks/yc-analytics.ipynb`

## Notes

- Tags are kept as-is (after basic normalization) without synonym merging
- Each company is counted only once per year, even if it has multiple health tags
- Location data is used exactly as provided in the source data
- Analysis focuses on batch year (when companies joined YC) rather than founding year

## License

Data scraped using [yc-scraper](https://github.com/corralm/yc-scraper). Please refer to their repository for data usage terms.

## Contributing

This is an analytical project. For improvements or suggestions, please open an issue or submit a pull request.
