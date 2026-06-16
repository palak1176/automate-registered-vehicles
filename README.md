# Georgia Registered Vehicle Statistics Automation
This project automates the collection of county-level vehicle registration statistics from the Georgia Department of Revenue e-Services website. Using Selenium, the script opens the registration statistics portal, iterates through all Georgia counties, extracts vehicle registration metrics, and saves the results as a structured CSV file.

## Features
- Automates browser interaction using Selenium
- Accesses the Georgia vehicle registration statistics portal
- Selects a user-specified year for data collection
- Iterates through all available Georgia counties
- Extracts total registered vehicles by county
- Collects vehicle category statistics, including:
    - Electric Vehicles (EVs)
    - Passenger Vehicles
    - Trucks
    - Trailers
    - Motorcycles
    - Buses
    - Other Vehicle Types
- Stores results in a pandas DataFrame
- Exports cleaned data to a CSV file
- Includes progress tracking with tqdm

## Technologies Used
- Python 3
- Selenium
- Pandas
- tqdm
- Jupyter Notebook

## Input Data
- The script retrieves data directly from the Georgia Department of Revenue e-Services website: https://eservices.drives.ga.gov/_/

## Output Data
- The script generates a CSV file containing county-level vehicle registration statistics: registered_vehicles_by_county_{year}.csv

## Usage
- Run the installation cell or install packages manually
- Open the Jupyter Notebook: jupyter notebook automate_registered_vehicles.ipynb
- Modify the year variable before running the collection process: year = 2023
- Run the notebook cells in order to launch the browser and open the Georgia registration statistics website to collect data
- After the data collection is complete, run the last cell to save the data as a CSV file in the current working directory

## Notes
- The website structure may change over time, which could require updates to Selenium element selectors.
- A stable internet connection is required while collecting data.
- Data availability depends on the Georgia Department of Revenue website.
- Scraping speed is controlled through built-in wait times to ensure reliable page interaction.
    - Can take 15 minutes to collect all data