# Data Cleaning Phase README

This README provides an overview of the data cleaning phase conducted on the dataset pertaining to conflicts in Europe, specifically focusing on Ukraine, spanning from February 24, 2022, to April 20, 2024.

## Steps Taken:

1. **Libraries Imported:**

   - Pandas (as pd)
   - NumPy (as np)
   - Matplotlib.pyplot (as plt)
   - Seaborn (as sns)
   - Plotly Express (as px)
   - os
   - Folium

2. **Setting Plot Size:**

   - Set the default figure size for Seaborn plots to (20, 6).

3. **Loading the Dataset:**

   - Loaded the conflict dataset from the specified path './data'.

4. **Data Exploration:**

   - Reviewed the first few rows of the dataset using `head()`.
   - Obtained information about the dataset using `info()`.
   - Generated descriptive statistics for the dataset using `describe()`.

5. **Creating a New DataFrame:**

   - Created a new DataFrame `expl_df` by making a copy of the original dataset.
   - Renamed the column 'event_id_cnty' to 'event_id'.
   - Selected relevant columns and filtered rows based on specific event types ('Explosions/Remote violence', 'Riots', 'Violence against civilians').
   - Renamed certain columns for clarity.

6. **Data Transformation:**

   - Converted the 'event_id' column values to integers by extracting the last 6 characters and converting them.
   - Reset the index of the DataFrame.

7. **Data Cleansing:**

   - Transformed values in the 'civilian_targeting' column according to the condition: 'Civilian targeting' to 'Yes', 'No' if NaN, else retain the original value.

8. **Saving the Cleaned Data:**
   - Exported the cleaned DataFrame to a CSV file named 'cleaned_data.csv' in the 'data' directory, excluding the index.

## File Structure:

- **cleaning.ipynb**: Jupyter Notebook containing the code for data cleaning.
- **cleaned_data.csv**: Cleaned dataset saved in CSV format.
- **README.md**: This file, providing an overview of the data cleaning process.

For more detailed information, please refer to the Jupyter Notebook `cleaning.ipynb`.
