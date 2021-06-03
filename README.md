# CWoLa-for-anomaly-detection

This repository contains a code with the CWoLa Hunting technique implementation for anomaly detection, and several additional codes to calculate the significance of the signal region excess after applying a cut on the classifer output.

The functionality of each code is detailed below:

**Main codes**
* CWoLa_scan_signal_m500.ipynb: implementation of the CWoLa Hunting technique for anomaly detection. The models are trained using this code.
* CWoLa_m500_pvalues_from_fit.ipynb: the classifier is deployed on test data. We calculate the significance of the signal region excess after applying a set of fixed cuts on the classifer output.
* CWoLa_m500_pvalues_based_on_SIC.ipynb: the classifier is deployed on test data. We calculate the significance of the signal region excess after applying a set of cuts on the classifer output. These cuts correspond to a series of working points of the ROC curve. More specifically, we calculate the threshold that corresponds to a fixed signal efficiency and take all the events on the test set above that threshold.

**Auxiliary codes**
* check_efficiency_after_epoch_end.ipynb: this piece of code is used on the main code to track the custom metric that we monitor durim training.
* get_p_value.ipynb: this piece of code contains the function that we use to calculate the p-value for the signal region excess.

