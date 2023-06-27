# AsYd - Asymmetry Detection

This repository contains an R notebook for analyzing and detecting asymmetries between two data sources: MDE and National Data. The notebook and app provide various tools for conducting a comprehensive analysis, including descriptive analysis and selective editing techniques, to identify and address the observed asymmetries.

## Getting Started

To use the code in this repository, follow the steps below:

### Prerequisites

Make sure you have the following R packages installed:

- dplyr
- DT
- glue
- ggplot2
- gridExtra
- htmltools
- kableExtra
- knitr
- plotly
- rlang
- shiny
- shinythemes
- writexl

You can install these packages using the following command:

```r
install.packages(c("dplyr", "DT", "glue", "ggplot2", "gridExtra", "htmltools", "kableExtra", "knitr", "plotly", "rlang", "shiny", "shinythemes", "writexl"))
```

### Installation

1. Clone this repository to your local machine or download it as a ZIP file and extract it.
2. Open the R notebook file (AsYd.Rmd) in RStudio or any other compatible R environment.

## Usage
### Data Preparation

1. Replace the placeholders "YYYY" and "MM" with the desired year and month in the code chunk named "configs". This will set the year and month values for your analysis.
```r
year  = "YYYY"
month = "MM"
```   
2. Specify the paths to your data input and output directories by updating the variables input_path and output_path in the "configs" code chunk.
```r
input_path   = "your_data_input_path"
output_path  = "your_output_path"
```  
3. Provide the filenames of your MDE and National data files by updating the variables filename_mde and filename_nat in the "configs" code chunk.
```r
filename_mde = "mde_data_filename.csv"
filename_nat = "national_data_filename.csv"
```
4. Make sure your MDE and National data files are in CSV format and contain the required columns: country code, product code, operator identifier, and a numeric value column. Adjust the variable mapping in the "variable mapping" code chunk if necessary:
```r
country_id  = "your_country_code"
product_id  = "your_product_code"
operator_id = "your_operator_identifier"
nat_value   = "your_national_value"
mde_value   = "your_mde_value"
```

### Notebook Usage

To run the notebook after completing the data preparation steps, simply click the "Run Document" button in RStudio. Once the notebook window opens, it is recommended to select the "Open in Browser" option to ensure proper functionality.

The notebook is structured into several sections, including an Exploratory Analysis section and an Asymmetry Detection section. The Asymmetry Detection section is further divided into three sub-sections: Systematic Errors, Selective Editing by Relative Contribution, and Selective Editing by the computation of a suspicion index.
