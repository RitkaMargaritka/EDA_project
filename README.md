# Exploratory Data Analysis  on King County Housing data

![King County Authority](pictures/KingCounty_pic.webp)

In this repository the king county dataset is analyzed.  
Relevant features are detected.  
### Task
Make a recommendation of at least 3 Houses for a chosen stakeholder. 

### File structure  

```root
├── /data (folder of all housing and modeling data)
│   ├── eda.csv (CSV imported through python)
│   └── kc_housing.csv (CSV imported through DBeaver, used for analysis)
├── /pictures (folder of visualizations used n the presentation)
├── 1_Fetching_the_data_eda.ipynb ( notebook used to import the data through python)
├── 2_EDA.ipynb (EDA and Feature Engineering workbook))
├── assignment.md (Generic task description)
└── README.md
```
### Outcome
Final customer presentation can be found here:
https://docs.google.com/presentation/d/1SzSBGX3HtLjGjlUOFl0tFgjEcfzGN3elthAtRLJwfV4/edit#slide=id.g261a3bbc3b8_0_65

The final result is a list of houses as recommendation for a chosen stakeholder. 

## Background

### Stakeholder ###

**Jennifer Montgomery** - Buyer: High budget, wants to show off, timing within a month, waterfront, renovated, high grades, resell within 1 year.

### Data ###
The data can be found on the kaggle platform.

In our case the data was preprocess and extracted from internal database. 
Column description.
- **id** - unique identified for a house
- **dateDate** - house was sold
- **pricePrice** - is prediction target
- **bedroomsNumber** - # of bedrooms
- **bathroomsNumber** - # of bathrooms
- **sqft_livingsquare** - footage of the home
- **sqft_lotsquare** - footage of the lot
- **floorsTotal** - floors (levels) in house
- **waterfront** - House which has a view to a waterfront
- **view** - Has been viewed
- **condition** - How good the condition is ( Overall )
- **grade** - overall grade given to the housing unit, based on King County grading system
- **sqft_above** - square footage of house apart from basement
- **sqft_basement** - square footage of the basement
- **yr_built** - Built Year
- **yr_renovated** - Year when house was renovated
- **zipcode** - zip
- **lat** - Latitude coordinate
- **long** - Longitude coordinate
- **sqft_living15** - The square footage of interior housing living space for the nearest 15 neighbors
- **sqft_lot15** - The square footage of the land lots of the nearest 15 neighbors





## Requirements

- pyenv
- python==3.11.3

## Setup

One of the first steps when starting any data science project is to create a virtual environment. For this project you have to create this environment from scratch yourself. However, you should be already familiar with the commands you will need to do so. The general workflow consists of... 

* setting the python version locally to 3.11.3
* creating a virtual environment using the `venv` module
* activating your newly created environment 
* upgrading `pip` (This step is not absolutely necessary, but will save you trouble when installing some packages.)
* installing the required packages via `pip`

At the end, you want to make sure that people who are interested in your project can create an identical environment on their own computer in order to be able to run your code without running into errors. Therefore you can create a `requirements file` and add it to your repository. You can create such a file by running the following command: 

```bash
pip freeze > requirements.txt
```

*Note: In rare case such a requirements file created with `pip freeze` might not ensure that another (especially M1 chip) user can install and execute it properly. This can happen if libraries need to be compiled (e.g. SciPy). Then it also depends on environment variables and the actual system libraries.*

### Unit testing (Optional)

If you write python scripts for your data processing methods, you can also write unit tests. In order to run the tests execute in terminal:

```bash
pytest
```

This command will execute all the functions in your project that start with the word **test**.


### Environment

This repo contains a requirements.txt file with a list of all the packages and dependencies you will need. Before you install the virtual environment, make sure to install postgresql if you haven't done it before.

```bash
brew update
brew install postgresql@14
```

In order to install the environment you can use the following commands:

```
pyenv local 3.11.3
python -m venv .venv
source .venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
```