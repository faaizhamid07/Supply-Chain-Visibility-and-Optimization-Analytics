# Dataset and Data Setup

This project uses AIS vessel-tracking data enriched with weather information.

## 1. Download the original dataset

Download the original dataset from Kaggle:

- **Dataset:** [AIS Data Complete Weather](https://www.kaggle.com/datasets/nadaemad2002/ais-data-complete-weather)
- **Publisher:** nadaemad2002

The raw dataset is not included in this GitHub repository because of its large file size. Review Kaggle's licence and usage conditions before reusing the dataset.

## 2. Clean and prepare the dataset

The Power BI report does **not** use the raw Kaggle CSV directly. It expects a cleaned/processed CSV named:

`ais_data_cleaned.csv`

After downloading the original dataset, perform the required data-cleaning and preprocessing so that the resulting CSV has the columns and structure expected by the Power BI model. Do not simply rename the raw CSV; it must be cleaned and prepared first.

## 3. Save the cleaned CSV to the expected location

The current Power BI semantic model contains this hardcoded file path:

`D:\ais_data_cleaned.csv`

To make the project open and refresh without changing its source query, save your cleaned file using this exact path:

1. Open the `D:\` drive on your computer.
2. Copy or move the processed CSV into the root of that drive.
3. Make sure the full file path is exactly:

   `D:\ais_data_cleaned.csv`

**Important:** The file must be named exactly `ais_data_cleaned.csv` and must be directly inside the `D:\` drive, not inside another folder. If your Windows installation does not have a `D:\` drive, you will need to change the CSV source path in Power BI Desktop to wherever you saved the cleaned file.

## 4. Open the Power BI project

1. Open the `dashboards/` folder.
2. Open `Supply Chain Visibility Optimization Analytics.pbip` in Power BI Desktop.
3. Once the project opens, refresh the data if required.

If Power BI reports that it cannot find `D:\ais_data_cleaned.csv`, confirm that the cleaned CSV exists at that exact location. Alternatively, update the file path in Power Query to match your own computer.

## Repository policy

Large raw and processed datasets are intentionally kept outside this repository to keep the Git history lightweight and avoid redistributing data unnecessarily. Each user must download and prepare the dataset locally.
