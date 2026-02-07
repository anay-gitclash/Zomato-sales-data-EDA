🍽️ Zomato Exploratory Data Analysis & Feature Engineering
📌 Project Overview

This project performs in-depth Exploratory Data Analysis (EDA) and Feature Engineering on the Zomato restaurant dataset to uncover insights related to restaurant distribution, ratings, pricing, cuisines, geography, currency, and service availability (online delivery & table booking).

The objective is to derive data-driven and business-relevant insights while demonstrating strong analytical reasoning and real-world data handling skills.

🎯 Objectives

Analyze restaurant distribution across countries and cities

Understand customer rating behavior

Study the impact of online delivery & table booking

Perform feature engineering to improve analytical clarity

Identify data bias, sparsity, and business limitations

Present insights using bar, scatter, pie, and ring (donut) charts

📂 Dataset Information

Source: Zomato public dataset

Records: ~9,000+ restaurants

Key Columns:

Restaurant Name

Country Code / Country

City & Locality

Cuisines

Average Cost for Two

Currency

Aggregate Rating

Rating Text & Color

Votes

Has Online Delivery

Has Table Booking

🛠️ Tools & Libraries Used

Python

Pandas – data manipulation

NumPy – numerical analysis

Matplotlib & Seaborn – data visualization

Jupyter Notebook

🧹 Data Cleaning & Preprocessing
Missing Value Analysis

The dataset is highly clean, with missing values found only in the Cuisines column.

Column	Missing Values
Cuisines	9

Missing cuisines were handled safely due to very low volume

No missing values in numerical, geographic, or rating-related features

🌍 Country-wise Analysis
Country Distribution

India dominates the dataset (~86%)

United States is the second-largest contributor

Other countries have limited representation

📌 Key Insight:
The dataset is heavily India-centric, and global comparisons without adjustment would be misleading.

💱 Currency-wise Analysis

Indian Rupees (INR) is the most dominant currency

US Dollar (USD) is second

Other currencies appear in very small volumes

📌 Important Insight:
Raw price comparisons across countries are not valid without currency normalization.
Therefore, pricing analysis was primarily conducted on INR-based restaurants.

🚚 Online Delivery Analysis (Country-wise)

India is the only country with large-scale online delivery availability

UAE shows limited online delivery

All other countries show no online delivery presence

📌 Key Insight:
Has Online Delivery is a country-dependent feature and was treated accordingly to avoid bias and zero-variance issues.

🏙️ City-level Analysis (NCR Focus)

A ring (donut) chart was used to analyze restaurant distribution across NCR cities:

New Delhi: ~69%

Gurgaon: ~14%

Noida: ~13%

Faridabad & Ghaziabad: Minimal presence

📌 Business Insight:
Zomato’s NCR presence is highly centralized, with potential expansion opportunities in underrepresented cities.

⭐ Aggregate Rating Analysis

Large spike at 0.0 ratings → unrated restaurants (cold-start problem)

Majority of restaurants fall between 2.8 – 3.6

High-rated restaurants (4.0+) are rare

📌 Key Insight:
Ratings show strong central tendency, and raw ratings were transformed into meaningful buckets.

🧩 Feature Engineering

To improve analysis and interpretability, the following features were engineered:

Rating-Based Features

Rating buckets:

Unrated (0.0)

Poor

Average

Good

Excellent

Binary feature: Is_Rated

Cuisine-Based Features

Handled missing cuisines

Split multi-cuisine entries

Created Cuisine_Count

Geographic Features

Country mapping from country codes

India vs Non-India binary feature

NCR city grouping (Core vs Peripheral)

Service Features

Binary encoding of:

Online Delivery

Table Booking

Country-conditional feature usage

These steps reduced noise, handled sparsity, and improved analytical reliability.

📊 Visualizations Used

Bar plots (country, city, cuisine distribution)

Scatter plots (cost vs rating, votes vs rating)

Box plots (pricing spread)

Pie charts (currency & delivery share)

Ring (donut) charts (NCR city distribution)

💡 Key Business Insights

Zomato data is India-focused

Online delivery is a major differentiator in India

High pricing does not guarantee high ratings

Restaurant density is highly concentrated in metro cities

Underrepresented regions show growth potential

🚀 How to Run the Project
git clone https://github.com/your-username/zomato-eda.git
cd zomato-eda
jupyter notebook


Run all notebook cells sequentially.

🧠 Skills Demonstrated

Exploratory Data Analysis (EDA)

Feature Engineering

Data Cleaning & Preprocessing

Data Visualization & Storytelling

Business Insight Extraction

Bias & Data Limitation Awareness

📌 Use Cases

Restaurant market analysis

Food delivery platform insights

Business expansion strategy

Data Science portfolio project

📬 Contact

Anay Pandey
📧 Email: your-email@example.com

🔗 GitHub: https://github.com/your-username

⭐ If you find this project useful, consider giving it a star!
