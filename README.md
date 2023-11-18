# PySIF: A Python Package for Solar-Induced Fluorescence Analysis
PySIF is a Python package that provides tools for processing and analyzing solar-induced fluorescence (SIF) data. SIF is a measure of the light emitted by plants during photosynthesis, and can be used as an indicator of plant health and productivity. It’s designed to work with raw files from the FloX instrument and processed files from the FloX GUI software. The toolkit provides functionalities such as wavelet coherence analysis, phase angle analysis, and various types of visualizations.

## Features
* Read and process raw SIF data from spectrometer files
* Calculate additional indices such as PRI, VPD, and CI
* Reshape and interpolate time series data
* Calculate multiscale rolling correlations between signals
* Perform wavelet coherence transform (WCT) and wavelet cross spectrum (WCS) analysis
* Plot and animate the results

## Dependencies
* pandas
* matplotlib
* glob
* numpy
* scipy
* seaborn
* pycwt

## Usage
To use PySIF, load the notebook and run through the installation and importation cells.

Then, use the functions to process and analyze the SIF data. For example, to create a DataFrame for the SIF data, use the create_SIF_dataframe function:

`SIF_data_df = create_SIF_dataframe(text_files, start_date='2023-05-14', end_date='2023', timezone='US/Central')`

This project uses the PyCWT library, which is licensed under the BSD 3-Clause License. See the LICENSE.txt file for more details.

## Acknowledgements

I would like to thank Dr. John Gamon, for his guidance and feedback throughout this project. I would also like to thank the Center for Advanced Land Management Information Technologies (CALMIT) and the McIntire-Stennis grant for providing the resources and funding for this project.

