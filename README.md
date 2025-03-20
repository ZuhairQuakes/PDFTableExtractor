# PDF Table Extractor

This Python script extracts numerical tables from PDF files and saves them as CSV files.

## Features

* Extracts tables from PDF files.
* Filters out non-numerical values, keeping only integers and floats.
* Saves each extracted table as a separate CSV file.
* Handles multiple PDF files within a folder.

## Requirements

* Python 3.x
* [Camelot](https://camelot-py.readthedocs.io/en/master/): `pip install camelot-py[cv]`
* [Pandas](https://pandas.pydata.org/): `pip install pandas`
* Optional: Ghostscript (required for Camelot)
    * [Instructions for installing Ghostscript](https://camelot-py.readthedocs.io/en/master/install.html#install-ghostscript)

## Installation

1.  Clone the repository:

    ```bash
    git clone <repository_url>
    cd <repository_name>
    ```

2.  Install the required Python packages:

    ```bash
    pip install -r requirements.txt
    ```
    (Note: You might need to create a `requirements.txt` file with `camelot-py[cv]` and `pandas`.)

3.  Install Ghostscript if you haven't already.  Follow the instructions in the Camelot documentation.

## Usage

1.  Place your PDF files in a folder (e.g., `papers`).
2.  Run the script:

    ```bash
    python your_script_name.py  # Replace your_script_name.py
    ```

3.  The extracted CSV files will be saved in the `extracted_numerical_tables` folder (or the folder you specified).

### Example

```python
# Example usage
pdf_folder = 'papers'  # Folder containing the PDF files
output_folder = 'extracted_numerical_tables'  # Folder to save the CSV files

if __name__ == "__main__":
    extract_numerical_tables_from_pdfs(pdf_folder, output_folder)
Inputpdf_folder: The path to the folder containing the PDF files you want to process.output_folder: The path to the folder where the extracted CSV files will be saved.OutputThe script will create one or more CSV files in the specified output folder. Each CSV file will contain the numerical data from a table found in the PDF. The filename of each CSV file will be in the format [pdf_filename]_table_[table_number]_numerical.csv.Error HandlingThe script includes error handling for the following:Errors reading PDF files.
