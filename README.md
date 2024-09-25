# SpaceX-Falcon-9-First-Stage-Landing-Prediction

## Overview
This project aims to predict the success of the Falcon 9 rocket's first-stage landing using historical data from SpaceX launches. The success of this landing is crucial as it allows for reusability, which significantly reduces the cost of space travel.

### Project Objective
The primary goal is to create a machine learning model capable of predicting whether the first stage of a Falcon 9 rocket will successfully land, making space missions more cost-efficient.

## Dataset
The dataset includes information on SpaceX launches such as:
- **Launch Date**
- **Launch Site**
- **Payload Mass (kg)**
- **Orbit**
- **Landing Outcome**

The dataset was collected from the following sources:
- **SpaceX API**: Used to extract data on historical launches via RESTful API requests.
- **Web Scraping**: Additional data collected from Wikipedia on Falcon 9 and Falcon Heavy launches.

The dataset and code for collection can be found in the `/data` and `/notebooks` directories, respectively.

## Project Structure

```
SpaceX-Falcon9-Landing-Prediction/
├── data/                    # Datasets used
│   ├── spacex_launch_data.csv
├── notebooks/               # Jupyter notebooks
│   ├── Data-Wrangling.ipynb
│   ├── EDA.ipynb
│   ├── Model-Building.ipynb
├── images/                  # Visualizations and diagrams
├── README.md                # Project documentation
├── requirements.txt         # Libraries required for the project
├── LICENSE                  # License information
└── .gitignore               # Files to ignore in Git
```

## Methodologies

### 1. Data Collection
- **SpaceX API**: Data was collected using API calls to the SpaceX database and parsed into a pandas DataFrame.
- **Web Scraping**: Additional data was scraped from Wikipedia using BeautifulSoup and requests.

### 2. Data Wrangling
- Cleaning the data, handling missing values, and selecting relevant features.
- Filtering the data to focus on Falcon 9 launches, removing irrelevant records.

### 3. Exploratory Data Analysis (EDA)
- **Data Visualizations**: Scatter plots, bar charts, and line plots were used to visualize relationships between variables like Flight Number, Launch Site, and Payload.
- **SQL Queries**: SQL was used for querying the dataset, performing tasks like calculating total payload, identifying launch sites, and analyzing success rates based on orbit types.

### 4. Machine Learning (Predictive Analysis)
- **Feature Engineering**: Created new features and labels to train the machine learning models.
- **Classification Models**: Tested multiple models such as:
  - Logistic Regression
  - K-Nearest Neighbors
  - Support Vector Machine (SVM)
  - Decision Trees
  
  Hyperparameter tuning was performed using GridSearchCV, and the best model was selected based on accuracy scores.

### 5. Visual Analytics & Dashboards
- Created interactive visualizations using Folium to map launch sites.
- Built a dashboard using Plotly Dash to display success rates for various launch sites and payload configurations.

## Results
The best model achieved an accuracy of **X%** in predicting the success of a Falcon 9 first-stage landing. Detailed results can be found in the Jupyter notebook `Model-Building.ipynb`.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/SpaceX-Falcon9-Landing-Prediction.git
   ```
2. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Jupyter notebooks to explore the data and build models.

## Notebooks Overview
- **Data-Wrangling.ipynb**: Cleans and preprocesses the data.
- **EDA.ipynb**: Exploratory data analysis and visualizations.
- **Model-Building.ipynb**: Model training, tuning, and evaluation.

## Conclusion
The project successfully demonstrates how machine learning models can be used to predict the outcome of SpaceX's first-stage landings. Through data wrangling, EDA, and predictive modeling, we were able to achieve a high level of accuracy in the predictions.
