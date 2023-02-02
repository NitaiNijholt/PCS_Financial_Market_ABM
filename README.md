# PCS_Financial_Market_ABM

Repo for Project Computational Science 2023

Linking agent-based models and stochastic models of financial markets - a reproduction of Feng et. al's 2012 paper by the same title

Team 5: 
Yonas Makoni - 14719576,
Calvin Law - 11306734,
Nitai Nijholt - 12709018,

Teacher: 
Professor Gábor Závodszky

## Installation & Run

1. Clone the repository.
2. Install the requirements: `pip install -r requirements.txt`.
3. Download & clean the data by running `DataImport_final.ipynb` in the `PCS_Financial_Market_ABM` folder as working directory. It will create a new folder called 'data' in the working directory.
4. Run `main_final.ipynb` (or if reviewing, `reproducible_figure.ipynb`)


If the `DataImport_final.ipynb.ipynb` downloading malfunctions for some reason, the data can be downloaded and extracted to this folder from the drive directly: https://drive.google.com/u/0/uc?id=1iuXLv3NpBLvxNpJwsYmLk4IX2TyjGtvP. In that event, please be sure to still run the data importer as it also cleans the data for use by the `main_final.ipynb`

## Structure

The PCS_Financial_Market_ABM folder contains all the code of the analysis.

    .
    ├── requirements.txt
    ├── README.md
    ├── main_final.ipynb 
    ├── DataImport_final.ipynb
    ├── reproducible_figure.ipynb
    ├── cumulative_distribution.png    # Constructed after running `reproducible_figure.ipynb`
    ├── used_ticker_list_dow.txt       # Constructed after running `DataImport_final.ipynb`
    ├── used_ticker_list.txt           # Constructed after running `DataImport_final.ipynb`
    └── data                           # Constructed after running `DataImport_final.ipynb`
    
Also, various dataframes are saved as .csv in both the data and main folders as the running of main_final.ipynb & DataImport_final.ipynb proceeds
        

## Project summary

In this project, Feng et al's (2012) paper ABM and stochastic model are implemented, analyzed for sensitivity to input parameters and compared against current empirical stock market return and volume data. The models reproduce 2 main features of Feng's paper, namely fat tailed return distributions and autocorrelation of returns (Long term memory) but the fits on the emperical data are imperfect, failing Kolmogrov Smirnov tests. Further extensions could include a more detailed parameter space exploration to improve the fit.

# Files

* `README.md`
> Running instructions 

* `requirements.txt `
> List of required packages which can be used to pip install them.

* `DataImport_final.ipynb`
> Data downloading & cleaning cleaning of the stock price data and constructing a data folder where cleaned files are put inside

* `main_final.ipynb `
> This file contains the code for running the simulations and does the analysis on it and also on the emperical data

* `used_ticker_list.txt`
> This file is a record of the S&P 500 stocks used

* `used_ticker_list_dow.txt `
> This file is a record of the DOW jones stocks used

* `reproducible_figure.ipynb`
> When ran, runs a simulation of each of the ABM, stochastic and stochastic with horizons model and outputs a simple reproducable figure called 'cumulative_distribution.png' showing a proof of concept of the model. One can also run the all main project files in the fashion described in the readme, but this version is skimmed down and saves bloat on the PC of the reviewer.

* `cumulative_distribution.png`
> The plot that should be aproximately reproduced for the codereview. 


* Various imported data .csv's, not mentioned in detail here


## References

- Feng, L., Li, B., Podobnik, B., Preis, T., & Stanley, H. E. (2012). Linking agent-based models and stochastic models of financial markets. Proceedings of the National Academy of Sciences, 109(22), 8388-8393.
- Wharton Research Data Services. "WRDS" wrds.wharton.upenn.edu, accessed 2023-01-29. S&P500 volume & shares outstanding data and DOW jones open & closing data.
- Yahoo Finance S&P 500 opening & closing Data: https://finance.yahoo.com/
- S&P 500 index clsoing data from NASDAQ: https://www.nasdaq.com/market-activity/index/spx/historical
