# Financial Planner

This project offers two financial analysis tools by using a single Jupyter notebook:

* A financial planner for emergencies. The members will be able to use this tool to visualize their current savings. The members can then determine if they have enough reserves for an emergency fund.

* A financial planner for retirement. This tool will forecast the performance of their retirement portfolio in 30 years. To do this, the tool will make an Alpaca API call via the Alpaca SDK to get historical price data for use in **Monte Carlo simulations**.

---

## Technologies

This analysis is implemented on the web-based interactive computer platform [Jupyter Notebook](https://jupyter.org/) using *Python*, Pandas, Matplotlib, NumPy, and consumes data from the [Alpaca API (v2) ](https://alpaca.markets/docs/trading/) 

📚 This project uses the following libraries to analyze and plot the data:


### OS

The OS module comes under Python's standard utility models and provides functions for interacting with the computer's operating system.

### Requests 

The Python Requests library helps you access data via APIs. To install the Requests library, run the following command:

``` bash
conda install -c anaconda requests
```

### JSON

This library puts the response (that is, the data) from an API into a human-readable format. To install the JSON library, check that your development environment is active, and then run the following command:

```
conda install -c jmcmurray json
```

### Dotenv

The python-dotenv library allow us to read key-value pairs from an environment file (.env) and add them as environment variables.

To install this library, run the following command in your terminal:
``` bash
pip install python-dotenv
```

### Alpaca SDK

Alpaca is an API for stock trading. With the Alpaca SDK, you can interact with the Alpaca API.

To install this SDK, run the following command in your terminal:

```
pip install alpaca-trade-api
```
**Important:** You need to generate your API credentials from the Alpaca API. If you don't have an account create one [here](https://app.alpaca.markets/signup) and get you API credentials (Key and secret)

### MCForecastTools

MCForecastTools is a library that will help us to create a **Monte Carlo simulation**

---

## Usage

* Clone the project from this repository to start using it. 
* Create a **.env** file in the root folder of your project. This file should contain the Alpaca API credentials. It should look like this:
```bash
ALPACA_API_KEY = "YOUR ALPACA API KEY"
ALPACA_SECRET_KEY = "YOUR ALPACA SECRET KEY"
```
⚡ **Important:** Make sure that you don't upload your credentials stored in your .env file. To do so, add the following to your **gitignore** file (if not already there)
```bash
 *.env
```
Using the user monthly income, crypto portfolio (BTC and ETH), stock and bond portfolio (AGG and SPY), to determine if the user has enough funds for and emergency fund. 

Later we run two Monte Carlo simulations with different weights for Stocks and Bonds (for 30 years and 10 years with 500 samples) to forecast the portfolio performance
