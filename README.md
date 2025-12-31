# NYC Airbnb Market Analysis – Private Rooms

## Project Overview
This project analyzes Airbnb listings in New York City to provide insights into the **short-term rental market**, with a focus on **private room listings**. The analysis combines multiple data sources in different formats (CSV, TSV, and Excel) to extract meaningful metrics for decision-making by a real estate start-up.

The main goal is to summarize:
- Review activity over time
- Number of private room listings
- Average listing prices

---
![NYC Airbnb Analysis](img/nyc.jpg)
---

## Business Objective
The insights from this analysis can help a real estate company:
- Understand trends in Airbnb reviews (earliest and most recent reviews)
- Identify the prevalence of private room listings in NYC
- Determine average pricing to assess market opportunities

This information is useful for property investment strategies, short-term rental planning, and market research.

---

## Datasets Used
The project combines three datasets from 2019 NYC Airbnb listings:

1. **`airbnb_price.csv`**  
   - `listing_id`: Unique listing identifier  
   - `price`: Nightly price in USD  
   - `nbhood_full`: Borough and neighborhood  

2. **`airbnb_room_type.xlsx`**  
   - `listing_id`: Unique listing identifier  
   - `description`: Listing description  
   - `room_type`: Type of room (Private room, Shared room, Entire home/apartment)  

3. **`airbnb_last_review.tsv`**  
   - `listing_id`: Unique listing identifier  
   - `host_name`: Host name  
   - `last_review`: Date of most recent review  

---

## Key Questions Answered
The analysis focuses on four main metrics:

1. **Earliest review date** (`first_reviewed`)  
2. **Most recent review date** (`last_reviewed`)  
3. **Number of private room listings** (`nb_private_rooms`)  
4. **Average listing price (USD)** (`avg_price`)

These metrics are combined into a single summary DataFrame called `review_dates` for simplicity and easy visualization.

---

## Analysis Steps
1. **Data Loading**
   - Read CSV, TSV, and Excel files into Pandas DataFrames.

2. **Data Cleaning**
   - Ensured all `listing_id` values match across datasets.
   - Converted `last_review` to datetime objects for accurate date comparison.

3. **Calculations**
   - Identified the earliest and latest review dates.
   - Counted all listings classified as **private rooms**.
   - Computed the average price of all listings, rounded to two decimal places.

4. **Summary**
   - Created a single-row DataFrame `review_dates` with columns:
     - `first_reviewed`
     - `last_reviewed`
     - `nb_private_rooms`
     - `avg_price`

---

## Example of Final Output

| first_reviewed | last_reviewed | nb_private_rooms | avg_price |
|----------------|---------------|-----------------|-----------|
| 2016-03-12     | 2019-12-31    | 1250            | 156.42    |

*Note: Values are illustrative.*

---

## Tools & Libraries
- Python
- Pandas (for data manipulation)
- Numpy

---

## Key Learnings
- Multiple file formats (CSV, TSV, Excel) can be combined seamlessly in Pandas.
- Converting date columns to datetime allows accurate comparisons.
- Summary metrics give a high-level view of the market, useful for business decisions.
- Structured outputs like a one-row DataFrame make reporting and dashboards easier.

---

## Potential Use Cases
- Real estate market research
- Short-term rental investment analysis
- Airbnb host trend analysis
- Dashboard-ready metrics for executive reporting
