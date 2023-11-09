# Alyterx-Data-Engineering-Project
#  Customer Sales by Department

## Overview

This Alteryx workflow is designed to analyze and report customer sales by department. The workflow performs data cleaning, transformation, and aggregation to provide the top 10 results per customer segment. The primary data sources are the sales and transaction files, which are joined based on the `customerId` column.

## Prerequisites

- **Alteryx Designer**: Make sure you have Alteryx Designer installed to run this workflow. You can download it from the [Alteryx website](https://www.alteryx.com/products/designer).

## Project Structure

The project is structured as follows:

- **Input Data Files**: Place your sales and transaction data files in the `data` directory. Ensure that the column names and data types are consistent with the provided sample files.

- **Alteryx Workflow**: The main workflow file is named `customer_sales_workflow.yxmd`. Open this file in Alteryx Designer to view and execute the workflow.

## Workflow Steps

1. **Data Cleaning**: The workflow starts by cleaning the data. It changes the data type of the `customerId`, `sales`, and `StoreNumber` columns. Additionally, it converts the `firstname` and `lastname` columns to uppercase. Rows with a value of "no" in the `responder` column are filtered out.

2. **Data Joining**: The sales file is joined with the transaction file based on the `customerId` column.

3. **Sorting**: The combined data is then sorted in descending order based on sales.

4. **Top 10 Results**: The workflow uses the Alteryx Sample tool to select the top 10 rows for each customer segment. It employs the GroupBy tool to group the data by customer segment.

5. **Output**: The final output is stored in the `output` directory. It contains a CSV file with the top 10 results per customer segment.

## How to Run

1. Open Alteryx Designer.

2. Open the workflow file (`Customer Sales.yxmd`).

3. Ensure that the input data files are in the `data` directory.

4. Run the workflow.

5. Check the `output` directory for the result CSV file.

## Note

- Make sure to customize the workflow if your data structure or file locations differ from the provided sample.

- If you encounter any issues or have questions, feel free to reach out to rutvikk99@gmail.com or https://www.linkedin.com/in/rutviksk/.

Happy analyzing!
