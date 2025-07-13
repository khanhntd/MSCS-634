# Weather Data Exploration and Preprocessing Lab

## 1. Purpose
The purpose of this lab was to explore, preprocess, and analyze a real-world weather dataset using Python and Jupyter Notebook. This included cleaning the data, visualizing important patterns, and applying basic statistical methods to understand the underlying trends in historical weather data.

## 2. Key Insights

- **Temperature Trends:**
  A line plot of temperature over time revealed clear fluctuations, suggesting seasonal or diurnal changes. The temperature exhibited patterns that align with common weather cycles.

- **Humidity Variation:**
  A box plot showed that humidity levels varied widely based on weather conditions. For example, rain-related summaries had higher humidity medians compared to clear or cloudy conditions.

- **Outlier Detection:**
  Using IQR, several extreme temperature values were identified and removed to reduce skewness in the data and improve the reliability of further analysis.

- **Correlation Findings:**
  A correlation matrix showed a strong negative correlation between temperature and humidity, and a mild positive correlation between wind speed and humidity.

- **Central Tendency & Dispersion:**
  The calculated mean and median provided a solid sense of average weather conditions. Standard deviation and IQR helped quantify variability in temperature and humidity.

## 3. Challenges and Decisions

- **Missing Values in 'Precip Type':**
  Some entries lacked precipitation type. These were filled using the mode of the column to preserve data size while maintaining consistency.

- **Outlier Handling:**
  Temperature values outside the IQR range were considered outliers and removed. This decision was made to reduce the influence of anomalies on visualizations and statistics.

- **Scaling and Binning:**
  Continuous variables like temperature and humidity were scaled using Min-Max normalization. Additionally, temperature was discretized into categories ('Cold', 'Moderate', 'Hot') to support categorical analysis.

- **Visualization Constraints:**
  Due to performance limitations, only a subset of the data (e.g., 500 rows) was used in visualizations such as time series plots for clarity and speed.

## 4. Tools Used

- Python (Pandas, Matplotlib, Seaborn, Scikit-learn)
- Jupyter Notebook
- Weather dataset sourced from Kaggle