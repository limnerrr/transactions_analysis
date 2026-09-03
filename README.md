# Transaction Dataset Analysis

## Project Overview

This project focuses on the analysis of a large-scale **transaction dataset** containing information about transactions, users, organizations, categories, payment methods, and transaction statuses.

The project follows an end-to-end data analytics workflow, starting with **data cleaning and preprocessing in Python**, followed by **SQL-based data analysis**, and finally the development of an interactive **Power BI dashboard**.

The main objective was to transform raw transactional data into meaningful insights about transaction activity, user behavior, organization performance, transaction outcomes, and temporal patterns.

## Project Workflow

```text
Raw Transaction Data
        ↓
Python
Data Cleaning & Preprocessing
        ↓
SQLite / SQL
Data Analysis & Querying
        ↓
Power BI
Data Modeling & Visualization
        ↓
Interactive Dashboard & Insights
```

## Dataset Structure

The project uses several interconnected tables:

* **Transactions** — main transaction-level fact table
* **Organizations** — organization information and category relationships
* **Categories** — business categories such as markets, electronics, and cosmetics
* **Operation Status** — transaction outcome information, including successful and refused operations

The Transactions table contains information such as transaction IDs, users, organizations, dates, transaction types, card information, and operation status IDs. Transaction types include **Return** and **Purchase**.

## 1. Data Cleaning & Preprocessing — Python

Python was used for the initial inspection, cleaning, and preprocessing of the raw transaction data.

### Main Steps

* Loaded the dataset into **Jupyter Notebook**
* Inspected the dataset structure and data types
* Removed irrelevant columns
* Performed duplicate checks
* Checked data quality before analysis
* Prepared the cleaned dataset for SQL analysis and Power BI

A total of **61 unnecessary columns** were removed during preprocessing, and no duplicate rows were found in the Transactions dataset.

### Tools & Libraries

* Python
* Pandas
* Jupyter Notebook

## 2. SQL Data Analysis

SQL was used to query and analyze the prepared transaction data in **SQLite**.

The analysis focused on identifying patterns in transaction activity, user behavior, organization performance, transaction statuses, and time-based trends.

### Organization & Category Analysis

* Top 10 organizations by transaction count
* Number of unique users by category
* Transaction distribution across categories
* Card vs. cardless transactions by organization
* Organization performance and transaction activity

### User Activity Analysis

* Top 5 users with the highest number of cards
* Top 10 users with the highest daily transaction count
* Top 5 users with the highest number of refused transactions
* User-level transaction activity and engagement

### Time-Based Analysis

* Yearly transaction trends by category
* Transaction distribution by hour of the day
* Transaction distribution by day of the week
* Identification of peak transaction periods

The SQL analysis showed a strong increase in transaction activity over the analyzed years, while weekends had lower transaction volumes compared with weekdays.

## 3. Power BI Dashboard

Power BI was used to build an interactive analytical dashboard based on the prepared dataset.

A relational data model was created using:

* Transactions
* Organizations
* Categories
* Operation Status
* Calendar

The Transactions table acts as the central fact table, while the other tables provide additional analytical dimensions. One-to-many relationships were established between the tables to support filtering and aggregation.

A Calendar table was also created using `CALENDARAUTO()` to support year, month, and day-based analysis and time-intelligence calculations.

### Dashboard Pages

#### General

Provides an overall view of transaction activity, including:

* Total transaction volume
* Card vs. cardless transactions
* Transaction trends
* Category performance
* Geographic activity
* Transaction success and refusal rates

#### Category

Analyzes transaction activity across business categories, including:

* Transaction volume by category
* User distribution
* Refusal rates
* Category trends over time

#### Operation

Focuses on transaction outcomes:

* Acknowledged transactions
* Refused transactions
* Transaction types
* Refusal patterns
* Potential areas for further investigation

#### Date

Provides time-based analysis:

* Yearly trends
* Monthly trends
* MoM growth
* YoY growth
* Last Month / Last Year comparisons
* Day-of-week analysis
* Hourly transaction patterns

#### User

Analyzes user behavior:

* Card usage
* User activity
* Category engagement
* User refusal rates
* Number of categories used by users

#### Organization

Provides organization-level insights:

* Transaction volume by organization
* User counts
* Refusal rates
* Organization performance
* Geographic distribution

## DAX & Power BI Techniques

The dashboard includes several DAX measures for dynamic analysis.

### Main DAX Functions

* `CALCULATE()`
* `FILTER()`
* `DIVIDE()`
* `COUNTROWS()`
* `COUNT()`
* `DISTINCTCOUNT()`
* `SUM()`
* `IF()`
* `SWITCH()`

These measures were used to calculate metrics such as:

* Total Transactions
* Refusal Rate
* Transactions with Card
* Transactions without Card
* Acknowledged Transactions
* Average Transactions per User

## Key Insights

The analysis revealed several important patterns:

* Transaction volume increased significantly between **2022 and 2024**.
* **October 22, 2024** was identified as the peak transaction day.
* More than **84% of transactions were conducted using cards**.
* Approximately **19% of transactions were unsuccessful/refused**.
* Transaction activity was highly concentrated in **Nərimanov**.
* The **market category** generated the highest transaction volume.
* **Electronics** showed the highest refusal percentages among the analyzed categories.
* Weekdays generally had higher transaction volumes than weekends.
* Certain users and card numbers showed unusually high refusal activity, highlighting potential areas for further investigation.

## Skills Demonstrated

This project demonstrates practical experience with:

* Data Cleaning & Preprocessing
* Exploratory Data Analysis
* SQL Data Analysis
* Relational Data Modeling
* Data Visualization
* Power BI Dashboard Development
* DAX Measures
* Time-Based Analysis
* User Behavior Analysis
* Business-Oriented Data Analysis
* Extracting actionable insights from transactional data

## Technologies

| Technology           | Purpose                                                |
| -------------------- | ------------------------------------------------------ |
| **Python**           | Data cleaning and preprocessing                        |
| **Pandas**           | Data manipulation and initial analysis                 |
| **SQLite / SQL**     | Data querying and analysis                             |
| **Power BI**         | Data modeling, visualization and dashboard development |
| **DAX**              | Measures and analytical calculations                   |
| **Jupyter Notebook** | Python-based data preparation and analysis             |

## Project Structure

```text
Transaction-Dataset-Analysis/
│
├── Python/
│   └── data_cleaning.ipynb
│
├── SQL/
│   └── transaction_analysis.sql
│
├── PowerBI/
│   └── transaction_dashboard.pbix
│
└── README.md
```

## Conclusion

This project demonstrates an end-to-end approach to analyzing transactional data — from raw data preparation and cleaning to SQL analysis, data modeling, visualization, and insight generation.

By combining **Python, SQL, and Power BI**, the project transforms raw transaction records into an interactive reporting solution that provides insights into transaction trends, user behavior, organization performance, payment methods, and operational outcomes.
