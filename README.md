# Airbnb Data Analysis

With the goal of studying information extraction from company data, this project presents an analysis of Airbnb data for the San Francisco, California region

### Informations about the data and data cleaning

[Inside Airbnb](http://insideairbnb.com/get-the-data/) is a platform dedicated to providing detailed information about lodging listings, allowing for in-depth analysis of rental market patterns and trends. The datasets available cover a variety of relevant information, including residence locations, property features, prices, availability, among others.

The Airbnb dataset for the city of San Francisco consists of **8056 entries** (rows) and **18 variables** (columns).

Predominantly, the dataset is composed of integer (int64) and object (object) data types. Some columns, such as `neighbourhood_group`, `reviews_per_month`, `last_review`, and `license`, contain float64 data types.

Some columns have a considerable number of unique values, such as `id` (8056), `longitude` (5898), `latitude` (5820). Regarding the `id` variable, it indicates that each data point is unique, while the high number of unique values in longitude and latitude is due to them being location variables. The dataset contains missing data in several columns.

The `neighbourhood_group` column is completely absent, and the `license` column has a missing rate of 36.80%. Other columns, such as `reviews_per_month` and `last_review`, also have a considerable proportion of missing values, reaching 23.39%.

**Dictionary of variables**

| Variable                      | Description                                                                                 |
|-------------------------------|---------------------------------------------------------------------------------------------|
| id                            | Unique identifier for the listing                                                           |
| name                          | Listing name                                                                                |
| host_id                       | Unique identifier for the property owner                                                     |
| host_name                     | Property owner's name                                                                       |
| neighbourhood_group           | Municipality to which the property belongs, geolocated by latitude and longitude coordinates |
| neighbourhood                 | Property's neighborhood                                                                     |
| latitude                      | Geographic latitude coordinate of the property                                                |
| longitude                     | Geographic longitude coordinate of the property                                               |
| room_type                     | Type of room offered for rental                                                             |
| price                         | Rental price per night                                                                      |
| minimum_nights                | Minimum number of nights to rent the property                                                 |
| number_of_reviews             | Number of reviews the property has                                                            |
| last_review                   | Date of the last review                                                                      |
| reviews_per_month             | Number of reviews per month                                                                  |
| calculated_host_listings_count| Number of properties by the same owner in the same city/region                                |
| availability_365              | Number of days available for rent in the next 365 days                                        |
| number_of_reviews_ltm         | Number of reviews in the last 12 months                                                       |
| license                       | Property registration number                                                                 |

### 1.1 Statistical description of variables

The variable `price`, which represents the price in dollars per night of the rental, shows an average of about \$228.00, with 75% of the values below \$232.00. However, the maximum price of \$25,000.00 and the considerable standard deviation of \$671.91 draw attention. This distribution suggests the presence of outliers that can impact the interpretation of the results.

Furthermore, the variable `minimum_nights` reveals that the average minimum nights for rental is approximately 24 nights, with 75% of the values below 30 nights. However, the maximum value recorded is 1,125 nights, a level outside the typical Airbnb rental pattern. This high value is notable and may be considered a possible outlier, requiring further analysis to understand its origin and impact on the study's conclusions.

Regarding the reviews, the average number of reviews per month (`reviews_per_month`) is approximately 2.06, with the maximum value of 162, considered high compared to the average, and the 75th percentile of 2.13, suggesting the presence of outliers. The same applies to the variable `number_of_reviews`, with an average of 44 and 75% of the data below 45. However, it has a maximum value of 877 and a standard deviation of 85.49, indicating the possible existence of outliers that deserve further investigation.

The variable `calculated_host_listings_count` reveals an average of 14 properties per user, but with a deviation of approximately 32 and a maximum value of 154. As for `number_of_reviews_ltm`, there is a maximum of 435, with an average of 6.89 and a standard deviation of 16.51. These data also point to the presence of discrepant values that can influence the analyses, highlighting the importance of considering these cases when interpreting the study's results.


## References Inspired

“12 bairros para conhecer em São Francisco,” Qual Viagem. Accessed: Feb. 01, 2024. [Online]. Available: https://www.qualviagem.com.br/12-bairros-para-conhecer-em-sao-francisco/

Análise de Dados em Python, (Nov. 12, 2022). Accessed: Feb. 01, 2024. [Online Video]. Available: https://www.youtube.com/watch?v=9n9bFWWBkLg

Curso rápido completo de Pandas - Parte 1, (Sep. 23, 2020). Accessed: Feb. 01, 2024. [Online Video]. Available: https://www.youtube.com/watch?v=6vpDSD1wchA

T. Corrêa, “Metodologia de análise de dados: um guia completo sobre o tema,” Blog da Ploomes. Accessed: Feb. 01, 2024. [Online]. Available: https://blog.ploomes.com/analise-de-dados/

T. AI, “Seaborn Tutorial 💹,” The Startup. Accessed: Feb. 01, 2024. [Online]. Available: https://medium.com/swlh/seaborn-tutorial-2e749e084ad6


