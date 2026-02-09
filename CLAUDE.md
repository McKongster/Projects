# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a personal workspace containing multiple independent projects — not a unified codebase. There is no shared build system, test suite, or CI/CD pipeline. Each subdirectory is self-contained.

## Project Layout

- **DataFolder/MasterDataStore/** — Research datasets and analysis projects
  - `nyc-taxi-data-master/` — NYC taxi/Uber trip analysis using PostgreSQL + PostGIS + R (see its README for full setup)
  - `2018-06-nyc-311-complaints-and-gentrification-master/` — BuzzFeed News 311 complaints analysis (Python/Jupyter, see its README)
  - `movielens/`, `ml-latest/` — MovieLens recommendation datasets
- **Python/** — Jupyter notebooks and Python experiments (data science, web scraping, file processing)
- **WaldorfWebSite/** — Static HTML/CSS consulting website (single-page, dark theme, no framework)
- **Rational/** — File deduplication analysis results

## Key Commands

### NYC Taxi Data Project
```bash
# Requires: PostgreSQL, PostGIS, R
cd DataFolder/MasterDataStore/nyc-taxi-data-master
./download_raw_data.sh        # Download raw CSV data (~267GB)
./initialize_database.sh      # Create PostgreSQL database and schema
./import_trip_data.sh         # Load trip records into database
```

### NYC 311 Complaints Project
```bash
cd DataFolder/MasterDataStore/2018-06-nyc-311-complaints-and-gentrification-master
pip install -r requirements.txt   # jupyter, pandas, geopandas, census, shapely, etc.
jupyter notebook                  # Run analysis notebooks
```

### Python Notebooks
```bash
cd Python
jupyter notebook    # or jupyter lab
```

## Languages and Tools

- **Python** (primary): pandas, numpy, matplotlib, BeautifulSoup, geopandas
- **SQL**: PostgreSQL with PostGIS extensions
- **Bash**: Data download and ETL scripts
- **HTML/CSS**: Static websites
- **R**: Statistical analysis (NYC taxi project)
