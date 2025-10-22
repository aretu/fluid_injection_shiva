# Shiva fluid injection experiments workflow
This repository contains the data reduction workflow of fluid injection experiments run with SHIVA apparatus (HPHT laboratory, INGV, Rome).

## Data repository document
All data included in this data repository is ancillary to the manuscript "Fault slip style in fluid injection experiments controlled by fault structure", to be submitted to "Communications Earth & Environment" by Aretusini and coauthors. 

The data consist in time series of high velocity friction experiments run with SHIVA (INGV, Rome) and numerical models. The data format is .mat, proprietary to Matlab, but they can be easily accessed with Python (see link). Each .mat file contains vectors of the measured variables when opened from Matlab, or dictionaries when opened using the scipy.loadmat() function. 

## Folder structure
```

|_ code
	|_ plots-multireactivation.ipynb
|_ data
	|_ experiments
		|_ shiva_perm_cycles
			|_ …
		|_ shiva_raw
		|_ shiva_red_jupyter
			|_ …
		|_ shiva_red_shivaUNIX
			|_ …
		|_ tables
			|_ experiment_stages.xlsx
|_ models
	|_ RSF_directmodels
		|_ inputparameters.xlsx
		|_ results
			|_ …
|_ plots
	|_ …
|_ results
	|_ permeability_results.xlsx
	|_ transmissivity_results.xlsx
```

## Workflow

![Workflow](https://github.com/aretu/fluid_injection_shiva/blob/main/worflow.png?raw=true)

Figure 1. Data reduction workflow. SHIVA raw data is not included. SHIVA red data (shivaUNIX and jupyter) are included in this data repository in separate folders. Numerical models are in models folder (the relation fin data to model is 1:n). The scripts to convert SHIVA raw data into SHIVA red data are at this link, we include the jupyter script with most of the workflow in scripts/plots-multireactivation.ipynb (from 2nd reduction to slicing and plotting), the scripts to obtain numerical models are at this link.

The most significant variables are presented in the following table (Table 1).

Table 1. The most significant variables.

| Variable name | Unit | data | Description |
| -------- | ------- | -------- | ------- |
| Time | ms | SHIVA | Shiva’s time |
| shear1 | MPa | SHIVA | Shear stress |
| vel | m/s | SHIVA | Equivalent velocity |
| slip | m | SHIVA | Equivalent slip |
| LVDT_high | mm | SHIVA | Axial shortening |