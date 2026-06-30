# Exploring Polarization: Spatial Clustering and Regionalization of the 2016 Vote

Final project for GEOG 585 (Quantitative Methods in Geography). Uses 2016 presidential election precinct-level results to detect spatial clustering and regionalization patterns in the electorate — framed as a tool a campaign data analyst might use to find partisan strongholds vs. contested areas.

The notebook itself has the full write-up (abstract, methods, discussion, conclusion) — `GEOG585_Project_Trevor.ipynb` is the place to actually read this project.

## What it does

Runs a state's precinct-level vote share through a series of spatial statistics: Global and Local Moran's I to detect clustering, LOSH to find "political islands," a custom polarization statistic (S), and two regionalization methods (Ward Spatial and SKATER) to partition the state into political regions. Default case study is Illinois, but the code can be pointed at any state in the source dataset.

## Why

Election results aren't randomly distributed in space — this project quantifies how clustered they are and uses that to identify where a campaign's spatial strategy should focus.

## How to run it

This was built in Google Colab against a personal Drive file and a custom module, so it's not a clone-and-run repo as-is. Easiest way to reproduce: open the notebook, then copy/paste the code cells into your own environment, swapping in your own data path and the `polarization1` module (linked in a comment in the notebook). Running cells out of Colab directly will fail on the Drive mount.

## Known limitations

- Requires Google Drive mount (Colab-specific) and a custom `polarization1` module not bundled in this repo.
- The CONUS-wide source geopackage isn't included (too large) — you'll need your own 2016 precinct-level election data.
- The script that built the cleaned CONUS geopackage from raw shapefiles isn't in this repo; the notebook starts from that already-cleaned file.

## Author

Trevor Tibbetts — GEOG 585
