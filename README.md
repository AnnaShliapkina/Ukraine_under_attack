# Project "Investigation of the War in Ukraine and Changes in Attacks and Fatalities"

## Project Description

This project investigates the war in Ukraine and changes in attacks and fatalities since the beginning of the war on February 24, 2022, to the present day. The data for analysis was obtained from [ACLED](https://acleddata.com), which contains information on all political violence events, demonstration events, and strategic developments in Ukraine.

## Dataset Description

For a detailed description of the dataset, including its structure, content, and potential use, please refer to the [README file](./data/README.md) located in the data folder.

## Steps Taken

The following steps were taken in the project:

### 1. Data Checking

Data was checked for missing values and duplicates.

### 2. Data Cleaning

#### Data Cleaning Phase

In the data cleaning phase, the raw dataset was processed to ensure consistency and reliability. The following steps were undertaken:

- **Loading and Exploration:**

  - The dataset was loaded into the environment using Pandas, and an initial exploration was conducted to understand its structure and content.

- **Data Cleaning and Transformation:**

  - Irrelevant or redundant columns were removed, and missing or inconsistent values were addressed.
  - Data types were adjusted, and columns were renamed for clarity.

- **Data Filtering:**

  - The dataset was filtered to include only relevant data points based on specific criteria or conditions.

- **Data Export:**
  - The cleaned dataset was exported to a CSV file for further analysis and modeling.

For a detailed overview of the data cleaning process and the code implementation, please refer to the `cleaning.ipynb` Jupyter Notebook.

### 3. Analysis

In this analysis phase, we delved deep into the conflict data related to Ukraine and uncovered several key insights:

- **Temporal Trends:** We observed distinct temporal patterns in conflict events, with certain months or periods experiencing higher levels of violence compared to others. This analysis helped identify potential seasonal variations or trends over time.

- **Spatial Distribution:** Through geographic analysis, we mapped the spatial distribution of conflict events across different regions of Ukraine. This revealed hotspots of violence and provided insights into the geographical spread of the conflict.

- **Event Types:** We analyzed the distribution of event types, including political violence, demonstrations, and strategic developments. This analysis allowed us to understand the nature and scope of the conflict in terms of the types of events involved.

- **Impact on Civilians:** By examining data on fatalities and civilian targeting, we assessed the impact of the conflict on civilian populations. This analysis highlighted the human cost of the conflict and the need for humanitarian interventions.

For detailed findings and visualizations, please refer to the [README file](./Analysis/README.md) located in the analysis folder.

### 4. Data Visualization

In this phase of the project, various visualizations were created to explore and analyze the conflict data in Ukraine. Some of the key visualizations include:

- [Monthly Fatalities Animation](https://annashliapkina.github.io/Ukraine_under_attack/charts/monthly_fatalities_animation.html): An animated map illustrating the temporal distribution of fatalities throughout the duration of the war. This visualization allows for the observation of patterns and trends in fatalities over time.

- [Fatalities Map](https://annashliapkina.github.io/Ukraine_under_attack/charts/fatalities_map.html): A map displaying the geographic locations of fatal events, with markers scaled based on the number of fatalities. This visualization provides insights into the spatial distribution of fatalities across different regions of Ukraine.

- [Heatmap](https://annashliapkina.github.io/Ukraine_under_attack/charts/heatmap.html): A heatmap representing the density of conflict events across various locations in Ukraine. This visualization highlights areas with a higher concentration of events, indicating potential hotspots of conflict activity.

These visualizations offer valuable insights into the dynamics of the war in Ukraine, enabling policymakers, researchers, and humanitarian organizations to better understand the patterns of violence and make informed decisions.

For additional visualizations and detailed analysis, please refer to the [README file](visualization/README.md) located in the visualization folder.

### 5. Machine Learning

#### Model

A logistic regression model was chosen and utilized for classifying event types. The model was trained and tested on the dataset, and its performance was evaluated using various metrics.

#### Usage

Follow these steps to utilize the project:

1. **Load Data**: Load the data from `cleaned_data.csv`.
2. **Feature Extraction and Encoding**: Extract features from the `event_date` column and encode categorical variables like `region`, `actor1`, and `actor2`.
3. **Select Features and Target Variable**: Choose relevant features and designate the target variable.
4. **Split Data**: Split the data into training and test sets.
5. **Train Model**: Train the logistic regression model on the training data.
6. **Make Predictions**: Use the trained model to predict on the test data.
7. **Evaluate Performance**: Assess the model's performance using metrics like accuracy, precision, recall, and F1-score.

#### Performance

The logistic regression model achieved an accuracy of approximately 98.68%. Performance varied across different event types, with high precision and recall for "Explosions/Remote violence" and lower performance for "Riots" and "Violence against civilians."

#### Conclusion

The logistic regression model demonstrates strong predictive capability for certain event types but faces challenges with others. Further refinement and exploration of alternative approaches are recommended to improve overall performance.

### File Structure:

- **Cleaning Phase**

  - `README.md`: Guide explaining the data cleaning process.
  - `cleaning.ipynb`: Jupyter Notebook with the code for data cleaning.

- **ML**

  - `README.md`: Description of the project and its structure for machine learning work.
  - `ML.ipynb`: Jupyter Notebook with the implementation of the machine learning project.

- **Charts**

  - `ACLED Event Types.jpg`: Image displaying ACLED event types.
  - `events_map.html`: Map showing different event types with colored markers and legend.
  - `fatalities_map.html`: Map displaying total fatalities in different locations with scaled markers based on the number of fatalities.
  - `heatmap.html`: Heatmap showing the density of conflict events in different locations.
  - `map.html`: Map displaying the first 10 events with markers.

- **Data**

  - `2022-02-24-2024-04-20-Europe-Ukraine.csv`: Original data file on conflict events in Ukraine and Europe.
  - `README.md`: Description of the dataset and its structure.
  - `cleaned_data.csv`: Cleaned data file saved in CSV format.

- **Analysis**

  - `README.md`: Description of the data analysis and its structure.
  - `analysis.ipynb`: Jupyter Notebook with the main data analysis code.
  - `more_analysis.ipynb`: Additional Jupyter Notebook with supplementary analysis.

- **Visualization**
  - `README.md`: Description of data visualizations and their usage.
  - `visualization.ipynb`: Jupyter Notebook with data visualization.

## Libraries Used

The following Python libraries were used in the project:

- pandas
- numpy
- matplotlib
- seaborn
- plotly.express
- folium
- sklearn
- os
