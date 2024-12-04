<div style="font-family: 'Times New Roman', Times, serif; font-size: 12pt; line-height: 1.5;">
</div>

# **1340 Fianl Project - README File**

## **Group 12**
Jiayi Cheng, 1011110049<br>
Mengyao Li, 1009902535<br>
Yiyang Qin, 1011790331

Instructor: Dr. Maher Elshakankiri

Course code: INF1340<br>
Course name: Programming for Data Science<br>
Program: Master of Information<br>
Faculty of Information<br>
University of Toronto

Date Created: <2024-11-19><br>
Date Modified: <2024-12-03>


## **Analyzing Potential Trends of COVID-19 in Different Countries**

This program analyzes a vast dataset of COVID-19, spanning from 2020-01-05 to 2024-08-04. It contains a comprehensive collection of data, focusing on both global trends and specific metrics related to countries. This dataset includes key statistics such as daily case counts, death rates, and vaccination rates over time. The main purpose is to visualize the dataset distribution and explore the potential relationships between variables, and develop predictive models to track and predict new COVID-19 cases, total deaths, and total mortality under different scenarios. This project combines three types of data analysis, descriptive, diagnostic, and predictive analysis, and different types of regression to gain insights into the dynamics and statistical variables of COVID-19 global trends.

The dataset is sourced from Kaggle and can be found her:
https://www.kaggle.com/datasets/assemelqirsh/covid19-dataset/data

## **Installation**
To run the analysis program, Python must be installed on the system.
The program makes use of a number of packages. Run the following commands to install them:

pip install pandas<br>
pip install matplotlib<br>
pip install seaborn<br>
pip install scipy<br>
pip install scikit-learn<br>
pip install statsmodels<br>
pip install imbalanced-learn<br>
pip install numpy

## **Usage**
1. Download the dataset from the provided Kaggle link
[https://www.kaggle.com/datasets/joebeachcapital/30000-spotify-songs?select=spotify_songs.csv](https://www.kaggle.com/datasets/assemelqirsh/covid19-dataset)
and save it as ‘covid_data.csv’.
2. Run the script using Python with the command:
INF 1340 Final Project.py
3. When prompted, enter the input file name: 'covid_data.csv'

## **Sample Output**
% python3 INF 1340 Final Project.py<br>
Enter the filepath: covid_data.csv

![AgePlot](https://github.com/user-attachments/assets/f38a2252-f612-4d87-8d1d-9e24ba45d123)
![model1](https://github.com/user-attachments/assets/35c1035d-78d1-4543-be27-50cf3389fd23)

#### t-Test Results by Country

| Country        | t-Test      | p-Value        |
|----------------|-------------|----------------|
| China          | 4.308525    | 1.720357e-05   |
| United States  | -2.985874   | 2.861959e-03   |
| Canada         | -2.931366   | 3.412896e-03   |
| Australia      | 12.812548   | 1.464569e-36   |
| Brazil         | -4.953047   | 8.021954e-07   |
| Afghanistan    | -4.237467   | 2.382806e-05   |
| Japan          | 10.440750   | 3.929048e-25   |
| South Korea    | 13.486493   | 9.042398e-40   |
| Denmark        | 7.590114    | 4.581275e-14   |
| India          | -1.959157   | 5.024011e-02   |

### Summary Statistics for Numerical Data

#### Descriptive Statistics
| Metric                         | Count      | Mean      | Std       | Min       | 25%       | 50%       | 75%       | Max       |
|--------------------------------|------------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|
| new_cases_smoothed             | 16748.000  | 0.003863  | 0.026177  | 0.000000  | 0.000007  | 0.000111  | 0.002241  | 1.000000  |
| new_deaths                     | 16748.000  | 0.003456  | 0.027282  | 0.000000  | 0.000000  | 0.000000  | 0.000000  | 1.000000  |
| total_deaths                   | 16748.000  | 0.152468  | 0.258711  | 0.000000  | 0.004070  | 0.020331  | 0.121925  | 1.000000  |
| new_cases_per_million          | 16748.000  | 0.002934  | 0.027776  | 0.000000  | 0.000000  | 0.000000  | 0.000000  | 1.000000  |
| positive_rate                  | 16748.000  | 0.038789  | 0.108996  | 0.000000  | 0.000000  | 0.000000  | 0.017935  | 1.000000  |
| new_vaccinations_smoothed      | 16748.000  | 0.020194  | 0.075450  | 0.000000  | 0.000000  | 0.000107  | 0.005042  | 1.000000  |
| total_deaths_per_million       | 16748.000  | 0.226209  | 0.292959  | 0.000000  | 0.019783  | 0.106581  | 0.303064  | 1.000000  |

#### Skewness
| Metric                         | Skewness   |
|--------------------------------|------------|
| new_cases_smoothed             | 29.055223  |
| new_deaths                     | 13.748682  |
| total_deaths                   | 1.808681   |
| new_cases_per_million          | 21.541965  |
| positive_rate                  | 4.555895   |
| new_vaccinations_smoothed      | 6.856526   |
| total_deaths_per_million       | 1.544060   |

#### Kurtosis
| Metric                         | Kurtosis   |
|--------------------------------|------------|
| new_cases_smoothed             | 999.952248 |
| new_deaths                     | 260.905745 |
| total_deaths                   | 2.200194   |
| new_cases_per_million          | 600.786020 |
| positive_rate                  | 24.376593  |
| new_vaccinations_smoothed      | 58.232979  |
| total_deaths_per_million       | 1.150047   |

#### Correlation Matrix
| Metric                         | new_cases_smoothed | new_deaths | total_deaths | new_cases_per_million | positive_rate | new_vaccinations_smoothed | total_deaths_per_million | days_since_2020_01_01 |
|--------------------------------|--------------------|------------|--------------|-----------------------|---------------|---------------------------|--------------------------|-----------------------|
| new_cases_smoothed             | 1.000000          | 0.097921   | 0.053151     | 0.112205              | 0.114308      | 0.044015                  | 0.017916                | -0.009336           |
| new_deaths                     | 0.097921          | 1.000000   | 0.093041     | 0.179235              | 0.058996      | 0.037649                  | 0.058937                | -0.069895           |
| total_deaths                   | 0.053151          | 0.093041   | 1.000000     | -0.018658             | -0.084023     | 0.042978                  | 0.807736                | 0.294356            |
| new_cases_per_million          | 0.112205          | 0.179235   | -0.018658    | 1.000000              | 0.202695      | -0.010914                 | -0.003006               | -0.003801           |
| positive_rate                  | 0.114308          | 0.058996   | -0.084023    | 0.202695              | 1.000000      | -0.007673                 | -0.098657               | -0.150140           |
| new_vaccinations_smoothed      | 0.044015          | 0.037649   | 0.042978     | -0.010914             | -0.007673     | 1.000000                  | 0.000000                | 0.000000            |
| total_deaths_per_million       | 0.017916          | 0.058937   | 0.807736     | -0.003006             | -0.098657     | 0.000000                  | 1.000000                | 0.000000            |
| days_since_2020_01_01          | -0.009336         | -0.069895  | 0.294356     | -0.003801             | -0.150140     | 0.000000                  | 0.000000                | 1.000000            |


![heatmap](https://github.com/user-attachments/assets/db5fa0ee-c2f3-4161-aeec-f59f3285c643)
![pair plot](https://github.com/user-attachments/assets/a5e5a13f-1684-4b04-91ab-5d72d2362028)


#### OLS Regression Results
![Linearplot](https://github.com/user-attachments/assets/bc887c71-96d1-4de8-a5f2-0d046b41e303)

| Metric                          | Value           |
|---------------------------------|-----------------|
| Dependent Variable              | case_fatality_rate |
| R-squared                       | 0.689           |
| Adjusted R-squared              | 0.534           |
| Model                           | OLS             |
| Method                          | Least Squares   |
| F-statistic                     | 4.432           |
| Prob (F-statistic)              | 0.0575          |
| Log-Likelihood                  | -8.3013         |
| No. Observations                | 10              |
| AIC                             | 24.60           |
| BIC                             | 25.81           |
| Df Residuals                    | 6               |
| Df Model                        | 3               |
| Covariance Type                 | nonrobust       |

#### Coefficients

| Variable                    | Coefficient | Std Err | t-value | P> absolute value of t | 0.25 | 0.75 |
|-----------------------------|-------------|---------|---------|------|----------|---------|
| const                       | 0.4582      | 1.299   | 0.353   | 0.736 | -2.720   | 3.637   |
| hospital_beds_per_thousand  | -0.0537     | 0.066   | -0.818  | 0.445 | -0.215   | 0.107   |
| diabetes_prevalence         | -0.0232     | 0.153   | -0.152  | 0.884 | -0.397   | 0.351   |
| cardiovasc_death_rate       | 0.0048      | 0.002   | 2.441   | 0.050 | -0.00001 | 0.010   |

#### Additional Metrics

| Metric           | Value    |
|-------------------|----------|
| Omnibus           | 0.670    |
| Prob(Omnibus)     | 0.715    |
| Jarque-Bera (JB)  | 0.432    |
| Skew              | -0.440   |
| Prob(JB)          | 0.806    |
| Kurtosis          | 2.487    |
| Durbin-Watson     | 1.948    |
| Condition Number  | 1.42e+03 |

![Model3](https://github.com/user-attachments/assets/a602e695-6341-4766-baea-a80483c7f6e0)
![Model2](https://github.com/user-attachments/assets/6687cf64-0538-48f5-bf06-e433083994a4)













