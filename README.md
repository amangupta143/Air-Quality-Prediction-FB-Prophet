# Air Quality Forecasting with Facebook Prophet

<img width="40%" align="right" src="https://github.com/amangupta143/Air-Quality-Prediction-FB-Prophet/assets/109453339/4450d726-4d8d-4afd-8ce8-e0b3e894982a"></img>

This project focuses on time series forecasting of air quality data using the Facebook Prophet algorithm. The dataset contains hourly averaged responses from an array of metal oxide chemical sensors deployed in an Italian city, along with ground truth concentrations for various pollutants provided by a co-located reference certified analyzer.

## Dataset

The dataset used in this project is the "Air Quality Dataset" from the UCI Machine Learning Repository. It was collected between March 2004 and February 2005 in an Italian city, providing a comprehensive set of readings over a full year. The dataset is provided in the `AirQualityUCI.csv` file.

## Preprocessing and Forecasting

The `Air_Quality_Forecasting.ipynb` Jupyter Notebook contains the code for preprocessing the data and performing time series forecasting using the Facebook Prophet algorithm.

### Preprocessing

The notebook includes a comprehensive preprocessing section that handles the following tasks:

- **Data Loading:** The script loads the dataset from the provided AirQualityUCI.csv file, handling the semicolon-separated values and comma-based decimal representation.
- **Missing Value Handling:** The script identifies and replaces missing values (tagged with -200) with NaN, and then fills the NaN values with the mean of the respective columns.
- **Date and Time Conversion:** The script converts the 'Date' column from 'DD/MM/YYYY' format to 'YYYY-MM-DD' format and the 'Time' column from 'HH.MM.SS' format to 'HH:MM:SS' format, suitable for time series analysis.
- **Feature Engineering:** A new 'ds' (date-time stamp) column is created by combining the 'Date' and 'Time' columns, and this column is converted to datetime format.
- **Target Variable Selection:** The script selects the 'Relative Humidity (RH)' column as the target variable for forecasting.

### Forecasting

The notebook includes a section for time series forecasting using the Facebook Prophet algorithm:

- **Data Preparation:** The script creates a new DataFrame with the 'ds' column as the datetime index and the 'RH' column as the target variable ('y').
- **Prophet Model Initialization:** The script initializes a new instance of the Facebook Prophet model.
- **Model Training:** The script trains the Prophet model on the prepared data.
- **Future Dataframe Generation:** The script creates a future dataframe with hourly intervals for the next 365 hours (approximately 15 days) using the `model.make_future_dataframe()` function.
- **Forecasting:** The script generates the forecast using the trained model and the future dataframe with `model.predict()`.
- **Visualization:** The script includes two visualization functions:

- **model.plot(forecast):** Plots the forecasted values and the actual values from the training data.
- **model.plot_components(forecast):** Plots the different components (trend, weekly, and yearly seasonality) of the time series data.



## Usage

To run the project, follow these steps:

1. Clone this repository:
   ```bash
   git clone https://github.com/amangupta143/Air-Quality-Prediction-FB-Prophet.git
2. Install the required dependencies (pandas, numpy, and fbprophet).
3. Open the `Air_Quality_Forecasting.ipynb` notebook in your preferred `Jupyter Notebook` environment.
4. Run the cells in the notebook to preprocess the data, train the Prophet model, and generate the forecast.

The notebook will display the visualizations and the forecasted values.

## Contributing

Contributions to this project are welcome. If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.

**To contribute:**
1. Fork the repository
2. Create a new branch for your feature or bug fix
3. Make your changes and commit them with descriptive commit messages
4. Push your changes to your forked repository
5. Submit a pull request to the main repository

## License

This project is licensed under the MIT License.

## Acknowledgments

The Air Quality dataset is provided by the UCI Machine Learning Repository: <a href="https://archive.ics.uci.edu/dataset/360/air+quality">Air Quality Data Set</a>. \
The Facebook Prophet library is developed and maintained by Facebook's Core Data Science team: Facebook Prophet.

<!-- Animated Line: -->

<img src="https://i.imgur.com/dBaSKWF.gif" height="20" width="100%">

Happy coding! 🚀

<!-- Footer Links -->
[![Portfolio](https://img.shields.io/badge/-Portfolio-red?style=flat&logo=appveyor&logoColor=white)](https://github.com/amangupta143)
[![Github](https://img.shields.io/badge/-Github-000?style=flat&logo=Github&logoColor=white)](https://github.com/amangupta143)
[![Linkedin](https://img.shields.io/badge/-LinkedIn-blue?style=flat&logo=Linkedin&logoColor=white)](https://www.linkedin.com/in/amangupta143/)
