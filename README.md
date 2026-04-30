# ARIA-E-H-Simulation
This repository contains four Python files, and they are used to generate the synthetic ARIA lesions into DHP,  four models are included: Hemorrhage, Superficial Siderosis, Effusion and Edema. Notice--A DHP dataset is required if user wish to activate these four programes.

# Overview
This project presents a computational framework for generating synthetic Amyloid-Related Imaging Abnormalities (ARIA), including ARIA-E (edema and effusion) and ARIA-H (hemorrhage and superficial siderosis), based on a Digital Human Phantom (DHP). Due to the limited availability of real ARIA datasets, especially following the recent introduction of Lecanemab, this work aims to create anatomically consistent synthetic lesions for research and analysis purposes. The approach is based on stacking axial PGM slices into a 3D volume and inserting parameterised ellipsoidal lesion models into specific tissue regions.

# Requirements:
Python 3.9+
NumPy

# Install dependencies:
pip install numpy

# How to run:
Four models have similar sturcture, so only the generation of Superficial Siderosis's model will be used as demonstration.
These are the input parameters that user needs to set:

cd "C:\Users\76897\Desktop\final year project" #Changes the working directory to the project folder where the Python script is located.

python extract_plane_siderosis.py ` #Runs the main Python script for generating superficial siderosis lesions and extracting a 2D slice.

  --folder "C:\Users\76897\Desktop\final year project\pgmdata" ` #Specifies the directory containing the DHP PGM slices, which will be stacked into a 3D volume.
  
  --plane z ` #Selects the axial (z-axis) plane for extraction.
  
  --index 60 ` #Defines which slice to extract (z = 60).
  
  --siderosis_y 299 ` #Sets the y-coordinate of the lesion centre.
  
  --siderosis_x 84 `#Sets the x-coordinate of the lesion centre.
  
  --siderosis_z 60 `#Sets the z-coordinate of the lesion centre.
  
  --a 30 `#Defines the ellipsoid radius along the y-axis (vertical direction).
  
  --b 23 `#Defines the ellipsoid radius along the x-axis (horizontal direction).
  
  --c 5 `#Defines the ellipsoid radius along the z-axis (depth direction).
  
  --siderosis_value 17 `#Sets the pixel intensity value of the lesion (low value to simulate hypointense regions in T2*-GRE).
  
  --out siderosis_z120.pgm #Specifies the output file name. The generated 2D slice with the simulated lesion will be saved as siderosis_z120.pgm.

  
<img width="431" height="106" alt="image" src="https://github.com/user-attachments/assets/1c6a5624-8e63-4c80-9034-d595690f9ec9" />

  
  
  
