# OpenCap-Shoulder-Analysis

## Overview
This repository contains Python scripts and other materials to analyze OpenCap data 
using OpenSim. We keep our main data (marker trajectories, videos, etc.) in a separate 
folder outside of this repository.

## External Data Location
We have an external folder ('C:\Users\*****\Documents\Research Work\OpenCap\opencap-core\Examples\Data\Latest_96df4120-f42a-4bed-9f01-242f71485dd4')
- CalibrationImages
- MarkerData
- OpenSimData
- Videos
- README.txt
- sessionMetadata.yaml

## Scripts
- `scripts/preprocess_marker_data.py`: Filters and cleans raw TRC files, storing the 
  processed outputs in a chosen directory or referencing them externally.

## How to Use
1. Clone this repository.
2. (Optional) Create and activate a Python virtual environment.
3. Adjust the script paths in `scripts/preprocess_marker_data.py` to point to your 
   external data location.
4. Run the scripts to generate processed marker data.
