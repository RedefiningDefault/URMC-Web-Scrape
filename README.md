# Web Scrape of University of Rochester Medical Center (URMC) Patient Lab Locations

Created to scrape the Patient Lab Locations of the University of Rochester Medical Center, this Jupyter Notebook cleans and formats the information and exports as a CSV file.

## Set Up and Configuration

1. Create and name a new folder
2. To that folder, save three files:
    - "URMC Web Scrape.ipynb
    - "2021-09-12 14:25_LabLocations.csv"
    - "urmc_env.yml"
3. Open a terminal window and navigate to your new folder
4. Type the following commands:

```
conda env create create --file urmc_env.yml
conda activate urmc_env
jupyter notebook
```

5. A web browser will open with teh Jupyter file tree. Click on your .ipynb notebook which will open in a new tab.

### Required Python Packages

To add required packages to your own environment:

```
conda install -c anaconda selenium              #to navigate to url
conda install -c conda-forge geckodriver        #to navigate web browser
conda install -c anaconda beautifulsoup4        #to parse html
conda install -c anaconda regex                 #to search by wildcards within html
conda install -c anaconda pandas                #to create dataframe and write to CSV
pip install datetime                            #to create timestamp on CSV exports for vesion control
conda install -c anaconda unicodedata           #to fix character encoding errors to improve human readability
conda install -c anaconda numpy                 #to get unique list values
conda install -c anaconda glob2                 #to find all CSV files in current directory
os                                              #to get filepath of CSV file
pip install openpyxl                            #required to read/write Excel files
```

## Unit Tests and Alerts

Cells that begin with #Unit Test are there to check things are running as expected. They will output a statement when run. If it says:

> Everything as expected.

you can keep going. Otherwise, this is your cue to do a manual check.

The cell which starts with #Check for Changes reads in the last .CSV file from the current working directory and compares it with the new scrape. This step will not work if the last .CSV file is not in the folder, or if you have made ***any*** changes to the old .CSV file. If you wish to edit an exported scrape, make a copy and save it to a sub-folder or change the file extension from .csv to .xlsx.

## Author

This Jupyter Notebook was developed by Kirsten Moreau of [Redefining Default LLC](www.redefining-default.com).

## License

This project is licensed under the MIT License. See the LICENSE.md file for details.
