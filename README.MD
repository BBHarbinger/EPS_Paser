# EPS Parser

### Author: Felix Yuzhou Sun

## Overview

This project involves the development of a versatile parser designed to extract Earnings Per Share (EPS) data from SEC EDGAR filings in HTML format. The parser is part of a DevOps Engineer Interview Project for Trexquant Investment LP. It systematically navigates complex financial documents, extracts the latest quarterly EPS values, and presents them in a structured CSV format.

## Project Structure

- **`parser.py`**: The core Python script that contains the parsing logic used to extract EPS data from the HTML files.
- **`main.ipynb`**: A Jupyter Notebook that walks through the entire process of setting up, running, and testing the parser, including code examples and explanations.
- **`output.csv`**: The generated CSV file containing the filename and the extracted EPS values for each filing.
- **`Training_Filings/`**: A directory containing the 50 example HTML files used for testing the parser.
- **`README.md`**: This file, providing an overview of the project, instructions for use, and additional details.
- **`requirements.txt`**: Lists all Python dependencies required to run the parser.

## Features

- **Robust Parsing**: The parser is designed to handle variations in HTML structure and formatting across different filings.
- **Keyword-Based Extraction**: Focuses on key financial terms like "Basic Earnings Per Share" and "Diluted Earnings Per Share" to locate and extract the relevant data.
- **Error Handling**: Includes mechanisms to handle missing data, unexpected formats, and negative EPS values.

## Usage

### Prerequisites

- Python 3.x
- Required Python libraries (listed in `requirements.txt`)

### Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/BBHarbinger/EPS_Paser.git
   cd EPS_Paser
   ```

2. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

### Running the Parser

You can either run the parser using the Python script or step through the process interactively using the Jupyter Notebook:

#### Option 1: Run via Python Script

```bash
python parser.py
```

This will parse the HTML files located in the `test_files/` directory and output the results to `output.csv`.

#### Option 2: Run via Jupyter Notebook

Open `main.ipynb` in Jupyter Notebook and run the cells step by step to see the parsing process in action. This notebook also provides explanations and examples.

```bash
jupyter notebook main.ipynb
```

## Output

The `output.csv` file will contain two columns:
- **`filename`**: The name of the HTML file processed.
- **`EPS`**: The extracted Earnings Per Share value.

Example:

```plaintext
filename,EPS
0001564590-20-019726.html,0.08
0000066570-20-000013.html,1.12
0000008947-20-000044.html,-0.41
```

## Testing and Validation

The parser has been tested across 50 example HTML files to ensure accuracy and reliability. The testing phase focused on handling variations in document structure and ensuring the correct extraction of EPS data, including handling of negative values and non-standard formats.

## Conclusion

This project demonstrates the ability to develop a robust parser for extracting financial data from complex documents. By focusing on common patterns, handling variations, and implementing strong error-handling mechanisms, the EPS Parser ensures accurate data extraction, supporting better financial analysis and decision-making.

## License

This project is for educational purposes and part of an interview project for Trexquant Investment LP. Redistribution or use of this code outside the scope of this project is not permitted without written consent.

