# Finance Tracker

This project is a simple finance tracking application written in Python. It allows users to record their financial transactions, categorize them as either income or expenses, and generate a summary of their transactions over a specified date range. The data is stored in a CSV file.

## Features

- Add new financial transactions with date, amount, category, and description.
- Store transactions in a CSV file.
- View transactions within a specified date range.
- Calculate total income, total expenses, and net savings for a given period.

## Tech Stack

- **Language:**

  - Python

- **Libraries:**
  - **pandas** – for data manipulation and analysis.
  - **datetime** – for handling date and time operations.
  - **csv** – for reading from and writing to CSV files.

## Code Overview

### `main.py`

- **Imports:**
  - `pandas`, `csv`, `datetime` for data manipulation and CSV file handling.
  - `data_entry` module for input functions (`get_amount`, `get_category`, `get_date`, `get_description`).
- **CSV Class:**

  - `initialize_csv()`: Checks if the CSV file exists, and creates one if it doesn't.
  - `add_entry()`: Adds a new entry to the CSV file.
  - `get_transactions()`: Retrieves transactions between a start and end date, and calculates income, expenses, and net savings.

- **Functions:**
  - `add()`: Prompts the user for transaction details and adds them to the CSV.
  - `main()`: Main function providing the command-line interface.

### `data_entry.py`

- **Functions:**
  - `get_date()`: Prompts the user for a date in `dd-mm-yyyy` format.
  - `get_amount()`: Prompts the user to enter a non-negative, non-zero amount.
  - `get_category()`: Allows the user to choose between "Income" and "Expense".
  - `get_description()`: Collects an optional description for the transaction.
