# OpenCap-Shoulder-Analysis

## Overview
This repository contains Jupyter Notebooks and Python scripts for analyzing OpenCap data using OpenSim. Our workflow is designed to:
- Preprocess raw marker trajectory data,
- Perform inverse kinematics,
- Refine musculoskeletal models by adding degrees of freedom,
- Set up and solve optimal control problems with OpenSim Moco,
- And finally, analyze and visualize the simulation results using the OpenSim GUI.

We store all the large OpenCap data (marker trajectories, videos, etc.) in a separate external folder so that the repository remains lightweight.

## External Data Location
Our OpenCap data is stored externally at: C:\Users*****\Documents\Research Work\OpenCap\opencap-core\Examples\Data\Latest_96df4120-f42a-4bed-9f01-242f71485dd4

### This folder contains:
- **CalibrationImages** (checkerboard images for camera calibration)
- **MarkerData** (raw TRC files)
- **OpenSimData**
  - **Model** (the scaled musculoskeletal model and associated geometry files)
  - **Kinematics** (processed MOT files)
- **Videos** (raw and processed video data, along with keypoint outputs)
- **README.txt** and **sessionMetadata.yaml**

## Notebooks
- **notebooks/preprocess_marker_data.ipynb**  
  This Jupyter Notebook loads raw TRC files, applies a low-pass Butterworth filter to clean the marker data, and includes inline visualizations to compare the raw versus the filtered data. The cleaned output is saved as new TRC files in your external data folder.
- *(Additional notebooks for further processing may be added periodically.)*

## How to Use
1. **Clone this repository** to your local machine.
2. **(Optional) Create and activate a Python virtual environment.**  
   For example, run:
   ```bash
   python -m venv venv
   ```
   and then activate it:
- On Windows: `venv\Scripts\activate`
- On macOS/Linux: `source venv/bin/activate`
3. **Modify the Notebook:**  
Open `notebooks/preprocess_marker_data.ipynb` in VSCode and update the data paths (e.g., `DATA_BASE_PATH`) to point to your external OpenCap data folder.
4. **Run the Notebook Cells:**  
Execute the cells to preprocess all raw TRC files (batch processing), generate cleaned marker data, and visualize the results to verify the filtering.
5. **Proceed with the Pipeline:**  
After preprocessing, continue with the subsequent steps in the analysis pipeline (inverse kinematics, model refinement, optimal control with OpenSim Moco, and analysis via the OpenSim GUI).

## Future Steps
- **Inverse Kinematics:** Use the OpenSim GUI to compute joint angles from the cleaned marker data.
- **Model Refinement:** Enhance your musculoskeletal model by adding extra degrees of freedom.
- **Optimal Control with Moco:** Set up and solve optimal control problems to determine muscle activations.
- **Analysis and Visualization:** Compare simulation results with experimental data and iterate as needed.



