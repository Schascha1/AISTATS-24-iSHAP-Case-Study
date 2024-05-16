# iSHAP post-hoc explanations: Covid-19 survival prediction
Supplementary case study for "Succinct Interaction-Aware Explanations", submission to Neurips-24.
Case study on a dataset of Covid-19 patients[^1] where a random forest model is trained to predict 
survival odds. We provide the explained prediction for each patient in a separate csv per method.

- For *SHAP*, we provide the explanation as a list of feature name + value and explained contribution
through the Shapley value.
- For *iSHAP*, we provide the explanation as a list of the sets of interacting features + values and 
explained contribution through their Shapley value, as well as for each set the contribution of
their interaction.
- For *NSHAP*, we provide all NSHAP contributions for all subsets up to size 4, i.e. all possible
combination of features with at most 4 components. Patient Index starts at 0 here, so that "0_nshap_covid.csv" 
has the first patient.

The csv files of the explanations used in the example from the paper are provided in "ishap_sample.csv",
"nshap_sample.csv" and "shap_sample.csv". The remaining files can be found indexed by their patient id
in the respective zip archives "covid-ishap", "covid-shap" and "covid-nshap".
Thank you for taking the time and effort to review!
    
[^1]: Lambert, Ben, et al. "Using patient biomarker time series to determine mortality risk in hospitalised COVID-19 patients: A comparative analysis across two New York hospitals." Plos one 17.8 (2022): e0272442.
