# Solar-Induced Fluorescence Analysis with Jupyter Notebook
PySIF is a Jupyter notebook that provides tools for processing and analyzing solar-induced fluorescence (SIF) as well as other spectral radiance and reflectance timeseries data.  SIF is a measure of the light emitted by plants during photosynthesis, and can be used as an indicator of plant health and productivity. It’s designed to work with raw files from the FloX instrument and processed files from the FloX GUI software. The toolkit provides functionalities such as wavelet coherence analysis, phase angle analysis, and various types of visualizations.

## Features
* Read and process raw SIF data from spectrometer files
* Calculate additional indices such as PRI, VPD, and CI
* Reshape and interpolate time series data
* Calculate multiscale rolling correlations between signals
* Perform wavelet coherence transform and partial wavelet coherence analysis
* Plot and animate the results

## Dependencies
* pandas
* matplotlib
* glob
* numpy
* scipy
* seaborn
* pycwt

## Data
The data used in this project are SIF measurements collected by the FloX instrument, which is a portable spectrometer that measures the radiance of the vegetation in the red and far-red bands. The data also include environmental variables, such as air temperature and relative humidity.

## Usage
To use the notebook, you need to load it in a Jupyter environment and run through the installation and importation cells. Then, you can use the functions to process and analyze the SIF data. For example, to create a DataFrame for the SIF data, use the create_SIF_dataframe function::

`SIF_data_df = create_SIF_dataframe(text_files, start_date='2023-05-14', end_date='2023', timezone='US/Central')`

Then the SIF_data_df can be used with various plotting functions like so:

`plot_rolling_corr(df=SIF_data_df, var1='PRI_s', var2='SIF_A_sfm [mW m-2nm-1sr-1]', win_len='6H', resample_len='18H', method='quantile',q=.95)`:

![rolling_corr_6H-PRI_s_SIF_A_sfm _18H](https://github.com/neillinehan/PySIF/assets/128750144/b4970142-ebb9-42b4-b320-6317fa898f1d)


## License

This project uses the PyCWT library, which is licensed under the BSD 3-Clause License. See the LICENSE.txt file for more details.

## Acknowledgements

I would like to thank Dr. John Gamon, for his guidance and feedback throughout this project. I would also like to thank the Center for Advanced Land Management Information Technologies (CALMIT) and the McIntire-Stennis grant for providing the resources and funding for this project.

