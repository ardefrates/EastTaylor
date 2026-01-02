# Code for “Water limitation dampens the effect of warming on transpiration and recharge in a high-elevation catchment”
Note that CW3E forcing files and model output files are not included due to size. CW3E forcing files may be subset from the CONUS2 grid using code at EastTaylor_inputs/subset_pf_inputs.ipynb. Model output .npy files saved in analysis notebooks are available upon request.

## Summary of files
#### subset_pf_inputs.ipynb
Using the subsettools package, subset the East-Taylor Watershed domain from the CONUS2 grid. Gather CW3E meteorological forcing files, static files, and CLM drivers. Changed start and end dates specified to gather input data for each of the water years studied, saving to the corresponding folder within EastTaylor_inputs/.

#### modify_forcing.ipynb
Apply a uniform $1.5^oC$ increase to the temperature forcing, changing the forcing file path accordingly to modify both WY2017 and WY2018.

#### runscripts/*.ipynb
Code for running ParFlow-CLM for the four meteorological scenarios studied, in addition to WY2003, which was run iteratively during spinup, replacing the starting pressure file with each run.

#### analysis_wy2003_newbounds.ipynb
For each WY2003 run used to spin up the model, read and save out subsurface storage, surface storage, overland flow, precipitation, and ET. Calculate the normalized change in storage for each run.

#### wy2017_1.5inc.ipynb
Save out all relevant ParFlow-CLM output for the WY2017 warming simulation. 

#### analysis_wy2017.ipynb
Save out all relevant ParFlow-CLM output for the WY2017 (wet year) baseline simulation. Analyze the effect of warming on SWE, saturation, evaporative fraction, transpiration, and recharge under wet conditions, generating corresponding figures.

#### wy2018_1.5inc.ipynb
Save out all relevant ParFlow-CLM output for the WY2018 warming simulation. 

#### analysis_wy2018.ipynb
Save out all relevant ParFlow-CLM output for the WY2018 (dry year) baseline simulation. Analyze the effect of warming on SWE, saturation, evaporative fraction, transpiration, and recharge under wet conditions, generating corresponding figures.
