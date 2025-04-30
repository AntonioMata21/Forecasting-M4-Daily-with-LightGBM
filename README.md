# Forecasting-M4-Daily-with-LightGBM
Code for the paper comparing LightGBM (M5 inspired) vs. ES-RNN (M4 winner) on M4 daily time series, analyzing the impact of trend on forecast performance.

# Download Data:
This study uses the dataset from the **M4 competition**, specifically the subset of **daily series** with more than 750 observations (N=2724). Download the data from the official source: [Link to official M4 Competition repository](https://github.com/Mcompetitions/M4-methods/tree/master/Dataset)

#Replication Files
To facilitate replication of the analysis presented in the paper, the following key data files generated during our study are included in this repository:
analysis_df.csv: This CSV file contains the combined results used for the main comparative analysis notebook (M4_Comparative_Analysis.ipynb). It includes the series ID, pre-calculated performance metrics (sMAPE, MAE, MAPE, RMSE) for both ES-RNN and the A5-inspired LightGBM model, the winning model's forecast correlation with actuals, a flag indicating the winning model (0=ES-RNN, 1=LightGBM based on sMAPE), and the calculated trend category for each series. Loading this single file allows direct execution of the analysis notebook, bypassing the need to run the raw data loading, forecast generation (for LGBM), and initial metric calculation steps.

DataStatisticalTest.csv: This file provides the data specifically formatted for replicating the statistical tests concerning the relationship between time series trend and forecast correlation.We originally conducted these tests using the PSPP software. This file allows users to easily replicate or verify these specific statistical findings using PSPP or other statistical software packages (like SPSS, R, etc.). It typically contains columns for the calculated trend category, and the relevant correlation coefficient.
