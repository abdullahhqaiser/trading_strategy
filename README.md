# Trading Strategy Automation

This project is designed to process trading data and calculate key trading insights, such as profit margins and indicators, based on predefined parameters. It automates the processing of trading data using Python, allowing for efficient analysis and storage of results.

## Features

- Reads raw trading data from an Excel file.
- Processes trading data based on Buy and Sell indicators.
- Calculates minimum and maximum values within the trading range.
- Computes profits based on buy price, sell price, and stop-loss conditions.
- Outputs processed results to a new sheet in the same Excel file.

## Project Structure

The project consists of two main files:

1. **`Main.py`**
   - Reads input parameters from a YAML configuration file (`params.yaml`).
   - Executes the main pipeline to process the trading data.
   - Leverages utility functions from `Common.py`.

2. **`Common.py`**
   - Contains helper functions for file I/O, data processing, and calculations.
   - Key functionalities:
     - Reading Excel files.
     - Identifying Buy and Sell indicators.
     - Equalizing indexes for processing.
     - Creating and writing to a processed DataFrame.
     - Calculating profit margins.
     - Saving processed results to an Excel file.

## Configuration File

The project uses a YAML configuration file (`params.yaml`) to specify:

- Column names for Buy and Sell indicators.
- Columns for the processed DataFrame.

### Example `params.yaml`

```yaml
buy_column: "Buy Indicator"
sell_column: "Sell Indicator"
processed_df_cols:
  - "buy"
  - "sell"
  - "stop_loss"
  - "min"
  - "max"
```
### usage
git clone https://github.com/your-repository/trading-strategy-automation.git
cd trading-strategy-automation
