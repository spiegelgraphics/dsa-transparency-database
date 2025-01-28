# dsa-transparency-database

Scripts for downloading, preprocessing and analyzing statements of reasons from the DSA transparency database.

# 1. Data Download (data_download.ipynb)
This script downloads daily reports from the DSA transparency database for specified platforms and months. It fetches zipped data files and saves them to a designated output directory. The script includes functions to handle the downloading process and manage the file structure.

Data source: https://transparency.dsa.ec.europa.eu/explore-data/download

API description: https://transparency.dsa.ec.europa.eu/page/api-documentation#statement-attributes

# 2. Data Preprocessing (data_preprocessing.ipynb)
This script preprocesses the downloaded data by categorizing and cleaning it. It assigns unique codes to long string values and stores these mappings in a lookup table. The processed data is then saved in an SQLite database for efficient querying and analysis.

# 3. Data Analysis (data_analysis.ipynb)
This script analyzes the preprocessed data stored in the SQLite database. It generates various metrics and visualizations to provide insights into the data. The script includes functions to execute SQL queries, decode category codes, and create visualizations using Altair.

## Required Libraries

- pandas
- datetime
- calendar
- requests
- os
- zipfile
- shutil
- sqlite3
- ast
- json
- numpy
- altair
