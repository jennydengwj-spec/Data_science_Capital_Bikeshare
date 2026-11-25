# Data_science_Capital_Bikeshare
Transportation equity and Capital Bikeshare usage in Washington, DC

# Who Does Capital Bikeshare Reach? Predicting Neighborhood Ridership to Find Where Use Falls Short

Georgetown University — Data Science final project (Fall 2026)
Team: Itzu Lin, Wenjie Deng, Rui Dong

## About

Capital Bikeshare keeps adding stations and bike lanes, but access shapes use, and use shapes where access goes next. A neighborhood with few stations will have few riders, and low ridership can then be misread as low demand. This project asks whether lower-income neighborhoods have less access to stations and bike lanes, and builds a model that predicts next month's ridership in every DC census tract using only information available before that month. Comparing predicted with actual ridership shows where use falls short of what a neighborhood's infrastructure and residents would suggest.

## Research questions

- **RQ1 (Describe the access gap).** Do lower-income neighborhoods have fewer nearby stations and less bike lane coverage?
- **RQ2 (Predict ridership).** How well can a tract's income, population, and bike infrastructure predict its ridership in the coming month, and where does actual ridership fall below that prediction?

## Data and design

- Unit of analysis: one 2020 census tract in one target month (206 tracts × 25 target months = 5,150 rows).
- Training: Nov 2024–Oct 2025. Test: Nov 2025–Oct 2026. Forecast: Nov 2026.
- Sources: Capital Bikeshare trip history; station locations (DC Open Data / GBFS); bike lanes (OpenStreetMap snapshots, checked against DDOT); ACS 5-year estimates; LEHD LODES workplace jobs.
- Every input uses the newest version published before the target month, so the model never sees information from the future.

## Repository structure

- `proposal.qmd` — project proposal (Quarto source)
- `proposal.html` — rendered proposal

## Tools

R with tidymodels and sf. All data are public.
