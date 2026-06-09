# ML Final Project: C2O Overnight Strategy

This repository contains the code and outputs for the BUSI70661 Machine Learning and Finance coursework project.

## Repository Structure

- `combine_feature.ipynb`  
  This notebook merges all raw datasets into the final stock-date modelling panel. It cleans and combines price data, fundamental features, earnings-related variables, short-interest variables, benchmark data, eligibility information, and cost-related inputs. The processed combined dataset is saved for later model training and backtesting.

- `model.ipynb`  
  This notebook runs the modelling and portfolio backtest. The user can specify the start year and end year for the test period. The notebook then trains the model using the rolling walk-forward procedure, generates out-of-sample predictions, constructs the long-short portfolio, applies the cost schedule, and outputs the strategy results, figures, and performance summaries.

- `figures/`  
  Contains figures used in the final report.

- `reports/`  
  Contains report-related outputs, including the QuantStats tear-sheet and final report files.

## How to Reproduce

1. Run `combine_feature.ipynb` first to generate and save the combined modelling dataset.
2. Run `model.ipynb`.
3. In `model.ipynb`, set the desired testing period by changing the start year and end year parameters.
4. Execute the notebook to produce model predictions, portfolio returns, figures, and performance summaries.

## Notes

The final model is a rolling random forest classifier for cross-sectional close-to-open return prediction. The backtest supports different AUM settings and applies the coursework-specified transaction cost schedule.
