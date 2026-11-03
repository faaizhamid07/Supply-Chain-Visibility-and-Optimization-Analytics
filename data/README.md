# Dataset and Data Setup

This project uses AIS vessel-tracking data enriched with weather information.

## Original dataset

The original source dataset is publicly available on Kaggle:

- **Dataset:** [AIS Data Complete Weather](https://www.kaggle.com/datasets/nadaemad2002/ais-data-complete-weather)
- **Publisher:** nadaemad2002

Download the dataset from Kaggle and review its licence and usage conditions before reusing or redistributing it. The raw dataset is not stored in this GitHub repository because of its large file size.

## Processed dataset required by the Power BI model

The Power BI semantic model currently reads a processed CSV named:

`ais_data_cleaned.csv`

This is the cleaned/processed file used to build the report. It is not necessarily identical to the original Kaggle download. If you are reproducing the project from the Kaggle source, you must run the project's data-cleaning/preprocessing workflow to produce a compatible `ais_data_cleaned.csv` with the columns expected by the semantic model.

## Local setup

1. Download the original dataset from the Kaggle link above.
2. Prepare the cleaned dataset named `ais_data_cleaned.csv` using the project's preprocessing workflow.
3. Open the Power BI project from the `dashboards/` directory.
4. In Power BI Desktop, update the CSV source in Power Query to point to the location of your local `ais_data_cleaned.csv`, if prompted.

> **Current source-path note:** The committed semantic model currently contains a local file reference to `D:\\ais_data_cleaned.csv`. This path is specific to the original developer's computer and will not exist on most other machines. Before refreshing the model on another computer, update the source path to the local location of your cleaned CSV.

## Repository policy

Large raw or processed datasets are intentionally kept outside this repository. This keeps the Git history lightweight and avoids redistributing data unnecessarily. Only download datasets from their original source and follow the source's licence and terms.
