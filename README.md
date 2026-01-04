# Customer Shopping Behavior Analysis 🛍️

## 📌 Project Overview
This project delves into customer shopping behavior, leveraging transactional data to uncover key insights into spending patterns, customer segmentation, product preferences, and subscription behavior. [cite_start]The ultimate goal is to translate these data-driven insights into actionable strategic business decisions[cite: 2, 3].

## 📂 Repository Structure
* **`cleanedData.ipynb`**: Python notebook for data loading, cleaning, feature engineering, and migration to PostgreSQL.
* **`Customer_behaviour.sql`**: SQL scripts used for querying the database to answer critical business questions.
* **`Customer-Shopping-Behavior-Analysis.pptx`**: Presentation summary of the project lifecycle, insights, and recommendations.
* **`customer_shopping_behavior.csv`**: (Ensure you upload the raw dataset if applicable) The raw dataset used for analysis.

## 🛠️ Tech Stack
* **Python**: Data cleaning and manipulation (Pandas, NumPy).
* **SQLAlchemy & Psycopg2**: Connecting Python to PostgreSQL.
* **PostgreSQL**: Database for structured query analysis.
* **SQL**: Executing complex queries to derive insights.
* [cite_start]**Power BI**: Interactive dashboard for data visualization[cite: 104].

## 📊 Dataset Description
[cite_start]The analysis is built upon a robust dataset comprising **3,900 distinct customer transactions** with **18 detailed features**, including[cite: 23, 24, 25]:
* **Demographics:** Age, Gender, Location.
* **Purchase Details:** Item Purchased, Category, Purchase Amount (USD), Size, Color, Season.
* [cite_start]**Behavioral Metrics:** Review Rating, Subscription Status, Shipping Type, Discount Applied, Previous Purchases, Frequency of Purchases[cite: 27, 28, 29].

## ⚙️ Methodology

### 1. Data Cleaning & Preparation (Python)
[cite_start]Using `cleanedData.ipynb`, the following steps were taken to ensure data integrity[cite: 33]:
* [cite_start]**Handling Missing Data:** Imputed missing values in the "Review Rating" column using the median rating specific to each product category[cite: 39].
* [cite_start]**Standardization:** Renamed columns to `snake_case` for consistency (e.g., `Purchase Amount (USD)` → `purchase_amount`)[cite: 42].
* **Feature Engineering:**
    * [cite_start]Created an `age_group` column (Young Adult, Adult, Middle Aged, Senior)[cite: 45].
    * [cite_start]Mapped `frequency_of_purchases` to a numerical `purchase_frequency_days` column[cite: 45].
* [cite_start]**Data Integration:** Dropped redundant columns (e.g., `promo_code_used`) and loaded the cleaned data into a PostgreSQL database named `customer_behaviour`[cite: 48].

### 2. Data Analysis (SQL)
Structured SQL queries were executed to answer specific business questions, such as:
* Revenue generation by gender.
* Impact of shipping types on purchase amounts.
* Top-performing products by rating and discount usage.
* Customer segmentation based on purchase history.

### 3. Visualization (Power BI)
An interactive dashboard was created to visualize:
* [cite_start]**Revenue by Category:** Clothing and Accessories dominate sales[cite: 118].
* [cite_start]**Demographics:** Young Adults and Middle-aged groups generate the highest revenue[cite: 120].
* [cite_start]**Subscription Trends:** 73% of customers are non-subscribers, presenting a growth opportunity[cite: 117].

## 💡 Key Insights
* [cite_start]**Gender Disparity:** Male customers contributed significantly more revenue ($157,890) compared to female customers ($75,191)[cite: 54].
* [cite_start]**Shipping Correlation:** Customers using **Express shipping** had a higher average purchase amount ($60.48) compared to Standard shipping[cite: 57].
* [cite_start]**Subscription Potential:** Non-subscribers contribute higher total revenue ($170k) than subscribers ($62k), but average spend is similar, indicating room for conversion[cite: 60].
* [cite_start]**Top Products:** Items like **Gloves, Sandals, and Boots** have the highest average ratings (>3.8)[cite: 66].
* [cite_start]**Discount Efficiency:** 839 customers used discounts yet maintained an above-average purchase amount, proving the effectiveness of targeted discounting[cite: 62].

## 🚀 Business Recommendations
[cite_start]Based on the analysis, the following strategies are recommended[cite: 123]:
1.  [cite_start]**Boost Subscriptions:** Target repeat buyers (specifically the 2,518 non-subscribers with >5 purchases) with exclusive benefits to drive conversions[cite: 76, 126].
2.  [cite_start]**Loyalty Programs:** Develop tiered loyalty programs to move "Returning" customers into the "Loyal" segment[cite: 128].
3.  [cite_start]**Targeted Marketing:** Focus ad spend on **Young Adult** and **Middle-aged** demographics and customers who prefer **Express shipping**, as they show higher purchasing power[cite: 79, 136].
4.  [cite_start]**Product Positioning:** Feature top-rated products (Gloves, Sandals) prominently in campaigns to leverage social proof[cite: 134].

## 💻 How to Run This Project
1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/RVenkateshS/customer-shopping-behavior.git](https://github.com/RVenkateshS/customer-shopping-behavior.git)
    ```
2.  **Install Python Dependencies:**
    ```bash
    pip install pandas sqlalchemy psycopg2-binary
    ```
3.  **Setup Database:**
    * Create a PostgreSQL database named `customer_behaviour`.
    * Update the credentials in `cleanedData.ipynb` (Variable: `connection_str`).
4.  **Run the Notebook:** Execute `cleanedData.ipynb` to clean data and populate the database.
5.  **Run SQL Analysis:** Use `Customer_behaviour.sql` in your SQL client (e.g., pgAdmin, DBeaver) to query the data.

---
*Created by Venkatesh Shashidhar*
