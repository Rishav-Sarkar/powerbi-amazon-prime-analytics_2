Amazon Prime Video Content Analysis – Power BI Dashboard
📌 Project Overview

This project showcases an interactive Power BI dashboard built to analyze the Amazon Prime Video content catalog.
The dashboard provides insights into content distribution, release trends, genres, ratings, and regional availability to support data-driven decision-making for OTT platforms.

This project demonstrates end-to-end Power BI development, including data preparation, DAX measures, and effective data visualization.

🎯 Business Objective

1. OTT platforms need clear visibility into their content libraries to:

2. Understand the balance between Movies and TV Shows

3. Track content growth over time

4. Identify popular genres and ratings

5. Analyze country-wise content contribution


This dashboard helps answer key business questions such as:

1. How is content distributed between Movies and TV Shows?

2. Which release years have the highest content volume?

3. What genres are most common on the platform?

4. Which countries contribute the most content?

5. How is content rated across the catalog?


📂 Dataset Information

1. File Name: amazon_prime_titles.csv

2. Total Records: 9,668

3. Total Columns: 12

4. Granularity: One row per title (Movie or TV Show)

5. Data Type: Public / anonymized dataset

Key Columns

1. show_id – Unique identifier

2. type – Movie or TV Show

3. title – Title name

4. country – Country of production

5. release_year – Year of release

6. rating – Content rating

7. listed_in – Genre(s)

8. duration – Runtime or seasons

9. date_added – Date added to Amazon Prime


🧹 Data Cleaning & Preparation

1. Data preparation was performed using Power Query, including:

2. Converting date_added to proper date format

3. Correcting data types for all columns

4. Handling missing values in country, director, and rating

5. Standardizing column names and formats

6. Parsing duration values for analysis



🏗️ Data Modeling

A single-table analytical model was used due to dataset size and scope

Logical dimensions were derived for:

1. Content Type

2. Release Year

3. Country

4. Genre

5. Rating

This approach ensures simplicity, good performance, and clear storytelling, while remaining scalable to a star schema for enterprise use cases.


📐 Key DAX Measures

Some of the core DAX measures used in the dashboard:

Total Titles =
COUNT(amazon_prime_titles[show_id])

Total Movies =
CALCULATE(
    [Total Titles],
    amazon_prime_titles[type] = "Movie"
)

Total TV Shows =
CALCULATE(
    [Total Titles],
    amazon_prime_titles[type] = "TV Show"
)

Movies % =
DIVIDE([Total Movies], [Total Titles], 0)

TV Shows % =
DIVIDE([Total TV Shows], [Total Titles], 0)

These measures enable dynamic filtering and interactive insights.

📊 Dashboard Features
A. Key Visuals

1. KPI Cards

2. Total Titles

3. Total Movies

B. Total TV Shows

1. Bar Charts

2. Titles by Release Year

3. Titles by Genre

4. Titles by Country

C. Donut / Bar Charts

1. Movies vs TV Shows

2. Rating Distribution

D. Interactive slicers for:

1. Content Type

2. Release Year

3. Country

4. Rating

E. Design Principles

1. Clean and minimal layout

2. Business-friendly color scheme

3. Consistent formatting

4. Focus on readability and insights

🔍 Key Insights

1. Movies form the majority of Amazon Prime’s content library

2. Content production increased significantly after 2010

3. Drama and Comedy are the most common genres

4. The United States contributes the highest number of titles

5. Most content falls under mainstream rating categories

🛠️ Tools & Technologies

1. Power BI Desktop

2. Power Query

3. DAX

4. Data Modeling

5. Data Visualization Best Practices

📁 Repository Structure

PowerBI-Amazon-Prime-Analytics/
│
├── Dataset/
│   └── amazon_prime_titles.csv
│
├── PowerBI/
│   └── Amazon_Prime_Content_Analysis_PowerBI.pbix
│
├── Screenshots/
│   ├── overview.png
│   ├── genre_analysis.png
│   └── country_distribution.png
│
└── README.md

🚀 How to Use

1. Download the .pbix file

2. Open it using Power BI Desktop

3. Refresh the dataset if required

4. Use slicers to explore insights interactively

📌 Use Case

This project is suitable for:

1. Power BI Developer portfolios

2. Data Analyst interviews

3. Business Intelligence demonstrations

4. Skill validation and learning

👤 Author

Rishav Sarkar
Power BI Developer | Data Analyst | Business Intelligence
