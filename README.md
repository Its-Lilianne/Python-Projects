# EXPLORATORY DATA ANALYSIS – CAR INVENTORY ANALYSIS PROJECT
The Car Inventory Analysis project is designed to explore and analyse key insights from a dataset containing details about various cars, including their make, model, colour, mileage, price, and cost. By applying data analysis and visualisation techniques using Pandas, Numpy, Matplotlib, and Seaborn, the project aims to uncover trends, relationships, and key patterns within the dataset.

## Objectives 
- Clean and preprocess the dataset to ensure data integrity. 
- Analyse the distribution of car prices to understand pricing trends. 
- Examine how mileage influences the price of a car. 
- Visualise the number of cars available by brand and colour. 
- Identify important insights that can help in pricing and inventory management.

## Expected Outcomes 
- A comprehensive understanding of the dataset through summary statistics. 
- Clear visual representations of car price distribution, mileage vs. price trends, and car counts by brand and colour. 
- Identification of key factors affecting car pricing and inventory trends. 
- Actionable insights for decision-making in car pricing and inventory planning.

## Key Questions 
- What is the general price distribution of cars in the inventory? 
- How does mileage impact the price of a car? 
- Which car brands are most commonly available in the inventory? 
- What are the most popular car colours in the dataset? 
- Are there any noticeable pricing trends based on car make and mileage?





# CAR INVENTORY ANALYSIS PROJECT
### Project Overview 
This Data Analysis Project aims to provide insight from a dataset containing details about various cars, including their make, model, colour, mileage, price, and cost. The project aims to uncover trends, relationships, and key patterns within the dataset.

### Tools
- Excel [Website](https://office.com)
- Jupyter Notebook

### Cleaning and Preprocessing the Dataset
  To ensure data integrity:
  1. Importing Libraries & Loading the Dataset
  2. Checking for missing values
  3. Removing duplicates (if any)
  4. Removing unwanted characters from numeric columns and converting to numbers

### Exploratory Data Analysis (EDA)
  Key Questions:
- What is the general price distribution of cars in the inventory?
- How does mileage impact the price of a car? 
- Which car brands are most commonly available in the inventory? 
- What are the most popular car colours in the dataset? 
- Are there any noticeable pricing trends based on car make and mileage?


### Data Analysis
Code Used

Import Library and Dataset

<pre> 
# import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

# Load the dataset
df = pd.read_excel('Car Inventory.xlsx')  # Ensure the Excel file is in the same folder or provide full path

# Display the first few rows
df.head()  
</pre>

Clean Dataset

<pre>
# Check for missing values
print(df.isnull().sum())

# Remove duplicates if any
df = df.drop_duplicates()

# Remove unwanted characters from numeric columns and convert to numbers
df['Price'] = df['Price'].replace('[\$,]', '', regex=True).astype(float)
df['Cost'] = df['Cost'].replace('[\$,]', '', regex=True).astype(float)
df['Mileage'] = df['Mileage'].replace('[,]', '', regex=True).astype(int)

# Verify data types
print(df.dtypes) 
</pre>


### Results

Summary of Key Insights from the Car Inventory Analysis Price Trends:
1. Car prices range: The car prices range widely, but most fall between $2,000 – $4,000. The average car price is around $3,000, indicating a focus on affordable used cars.
2. Mileage vs. Price: Cars with lower mileage generally cost more, which is expected. There are a few high-mileage vehicles priced higher, possibly due to brand value or condition.
3. Popular Brands: The most common brands in the inventory are Toyota, Ford, and Chevrolet. This may suggest either high customer demand or dealer preference for these brands.
4. Car Colour Preferences: Colours like Silver, Black, and White dominate the inventory. This can be useful in restocking and marketing based on colour popularity.
5. Profitability: The average profit margin differs by brand. Brands like Ford and Chevrolet seem to have higher average profits compared to others.


### Recommendation

We recommend the following: 
1. Inventory Planning:
   - Continue focusing on the $2k–$4k price range to attract cost-conscious buyers.
   - Maintain a balance of affordable vehicles with low mileage to appeal to both price and quality seekers.
  
2. Targeted Procurement:
   - Prioritise Ford and Chevrolet for stock replenishment due to higher profitability.
   - Evaluate conditions of high-mileage but high-priced vehicles for brand-based premium pricing strategy.
  
3. Colour Stock Strategy:
   - Maintain a strong stock of Silver, Black, and White vehicles — they sell well and appeal to a broad customer base.
   - Consider bundling marketing strategies (ads, promotions) around these colours.

5. Brand-Level Promotions:
   - Promote Toyota, Ford, and Chevrolet heavily — their popularity means faster sales turnover.
   - Consider extended warranty or service packages for these brands to boost sales volume.
     
6. Data-Driven Pricing:
   - Implement a pricing model based on mileage, brand, and colour popularity to optimise profit while staying competitive.

7. Market Research Extension:
   - Regularly monitor customer preferences and competitor pricing to keep the inventory aligned with market demand.
  

### Limitations

A limitation in data analysis reporting refers to any factor that restricts, weakens, or challenges the accuracy, scope, or generalizability of the analysis results.

While the analysis provided key insights into car pricing and brand performance, limitations such as missing mileage data and a lack of customer purchase history may have affected the completeness of the conclusions. Future analysis should aim to include these data points for a more comprehensive overview.”


### References

[Car Dataset](https://docs.google.com/spreadsheets/d/148gzCAxQno4wlIj_tzgUIyDTG8y4ifRr/edit?usp=sharing&ouid=107969485968939728677&rtpof=true&sd=true)


## Table of Contents

- [Project Overview](#project-overview)
- [Results](#results)
- [Recommendation](#recommendation)
