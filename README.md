# CWoLa and Autoencoders for Anomaly Detection

This repository contains the codes with the implementation of the CWoLa Hunting and Autoencoder techniques for anomaly detection, and several additional codes to calculate the significance of the signal region excess after applying a cut on the classifers output.

These codes have been used to produce the results presented in the publication *Comparing Weak- and Unsupervised Methods for Resonant Anomaly Detection*, which can be found here: [arXiv:2104.02092](https://arxiv.org/abs/2104.02092). The data used to produced these results was generated in the context of the LHC Olympics 2020 and can be downloaded from [this](https://zenodo.org/record/4536377) Zenodo repository.

The functionality of each code is detailed below:

## Main codes
* CWoLa_scan_signal_m500.ipynb: implementation of the CWoLa Hunting technique for anomaly detection. The models are trained using this code.
* CWoLa_m500_SIC_curves.ipynb: we calculate the averaged SIC curve for each S/B benchmark.
* CWoLa_m500_pvalues_from_fit.ipynb: the classifier is deployed on test data. We calculate the significance of the signal region excess after applying a set of fixed cuts on the classifer output.
* CWoLa_m500_pvalues_based_on_SIC.ipynb: the classifier is deployed on test data. We calculate the significance of the signal region excess after applying a set of cuts on the classifer output. These cuts correspond to a set of working points of the ROC curve and are tuned using the peak of the SIC curve. More specifically, we take the signal efficiencies that correspond to the peak(s) of the SIC curve, we calculate the thresholds for these fixed signal efficiencies, and then take all the events on the test set above that threshold.

**Auxiliary codes**
* check_efficiency_after_epoch_end.ipynb: this piece of code is used on the main code to track the custom metric that we monitor durim training.
* get_p_value.ipynb: this piece of code contains the function that we use to calculate the p-value for the signal region excess.

