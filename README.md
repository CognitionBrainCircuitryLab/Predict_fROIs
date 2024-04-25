# Predict fROIs from Connectivity
Github repository to accompany "Predicting High-level Visual Areas in the Absence of Task fMRI" by Molloy, Saygin & Osher (under review). 

## Version 1: release of final trained model 

The repository currently contains the search spaces from Julian et al. 2012 and the final trained model from Molloy et al. (under review) sufficient for anyone computationally savvy to predict high-level visual fROIs from their own resting state data. 

The Julian et al. search spaces are included as .label files for the 18 fROIs in the directory 'Search Spaces'. 
`finalmodel.mat` contains the following variables:
- `allrois` is an 18 item vector of the abbreviations for each fROI in order.
- `alltargets` is a structure with a field for each fROI giving the list of the names of the 179 regions from Glasser et al., and labels for x, y, z, curvature, and thickness.
- `bestbetas` is a 185 (total predictors/targets) x 18 (total number of fROIs) matrix of the final model's β values.
- `bestlambdas` is an 18 item vector with the final model's λ value for each fROI.

### To-do's for later versions
- [ ] script to apply models, assuming functional connectivity is computed and in correct order
- [ ]  script to compute functional connectivity and wrap it all together
