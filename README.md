# CityGML-CityJSON
## Practice of citygml-tools and cjio.
* Convert the CityGML file into CityJSON with citygml-tools.
* Validate the CityJSON file with cjio command line. Upgrade the file and validate it.
* Python practice to retrieve data of buildings from the CityJSON file.

## Project: Building Height Analysis from CityJSON Data
### Overview
This project provides a Python script to analyze building height data from a CityJSON file. It generates a distribution of buildings based on their heights and visualizes the data in a pie chart. The script performs the following tasks:

* Loads a CityJSON file containing city object data.
* Extracts building height information.
* Categorizes buildings into height ranges.
* Creates a pie chart to visualize the distribution of building heights.
### Requirements
* Libraries:

    os

    json

    pandas

    matplotlib

### File Structure

* Vienna_102081_v20.city.json: The input CityJSON file containing city object data. It has been converted and upgraded from the CityGML file with citygml-tools and cjio command line.
* main.py: The main Python script that processes the CityJSON data, calculates height distributions, and generates a pie chart.

### Functions
#### 1. load_cj_file(file_path):

* Loads the CityJSON file from the specified path.
* Returns the parsed JSON data.

#### 2. buildings_heights(cj):

* Extracts building and building part heights from the CityJSON data.
* Returns a dictionary of building IDs and their corresponding heights.

#### 3. height_distribution(bd_heights):

* Categorizes the buildings based on their heights into 4 categories:

    '0-10m',

    '10-20m',

    '20-30m',

    '30m+'

* Returns a pandas DataFrame showing the distribution of buildings across these height categories.

#### 4. pie_chart(hd):

* Generates a pie chart based on the height distribution.

* Displays the chart with labeled height categories and percentage of buildings in each category.

#### 5. main(file_path):

* Integrates the above functions to process a CityJSON file, calculate building height distributions, and display a pie chart.
