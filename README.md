This repository contains a script to process an Excel file and filter data based on specific criteria.

## Prerequisites

You first need to create an Excel file with a first column "Image" containing the name of each image, and a second column "Atlas_X" containing the CCFv3 coordinates of each detection extracted from QuPath.

## Install

- Python 3.11
- pandas

## Installation

3. Install the required packages:
    ```sh
    pip install -r requirements.txt
    ```
    
## Script Description

- **process_data.py**: This script loads data from an Excel file, calculates the mean of CCFv3 X coordiantes values for each image, filters the means within a specified range, and saves the filtered data to a new Excel file.
