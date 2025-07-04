# DSA-Capstone-Project-Amazon-Product-Review-Analysis
This project was completed as part of my data analysis training and focuses on analyzing Amazon product and customer review data using Microsoft Excel. 
## Dataset Overview
- **Total Records:** 1,465
- **Total Fields:** 16
- Product details, prices, discounts, ratings, and customer engagement data.
-
  ## Analysis Objectives
Using pivot tables, and calculated columns, I analyzed:
1. What is the average discount percentage by category?
2. How many products are listed in each category?
3. What is the total number of reviews per category?
4. Which products have the highest average ratings?
5. What is the average actual vs discounted price per category?
6. Which products have the highest number of reviews?
7. How many products have a discount of 50% or more?
8. How are product ratings distributed?
9. What is the total potential revenue (actual price × rating count) by category?
10. What is the number of unique products by price range?
11. What is the relationship between average rating and discount percentage?
12. How many products have fewer than 1,000 reviews?
13. Which categories offer the highest discounts?
14. What are the top 5 products by rating + number of reviews combined?
##Tools Used
- **Microsoft Excel**
  - Pivot Tables
  - Calculated Columns
  - Basic Charts (bar, line, scatter)
- **GitHub** – Documentation and version control

    ## Amazon Product Analysis – Steps
- Average Discount Percentage by Product Category
    - Added calculated column: = (Actual Price - Discounted Price) / Actual Price * 100
    - Created Pivot Table: Rows: Category, Values: Discount % → Average

- Number of Products in Each Category
    - Pivot Table:Rows: Category. Values: Product Name → Count (Distinct)
- Total Number of Reviews per Category
    - Pivot Table: Rows: Category. Values: Rating Count → Sum
-  Products with the Highest Average Ratings
    - Sorted dataset by Average Rating (Descending)
    - Selected top-rated products
- Average Actual Price vs Discounted Price by Category
    - Pivot Table:Rows: Category ,Values: Actual Price → Average, Discounted Price → Average
-  Products with the Highest Number of Reviews
    - Sorted Rating Count column in descending order
-  Products with 50% or More Discounts
    - Added calculated column:=IF(Discount % >= 50, "Yes", "No")
    - Used COUNTIF to count products
-  Distribution of Product Ratings
    - Pivot Table: Rows: Rating (rounded if needed), Values: Product Name → Count
-  Total Potential Revenue by Category
    - Added calculated column:= Actual Price * Rating Count
    - Pivot Table:Rows: Category, Values: Potential Revenue → Sum
-  Unique Products per Price Range
     - Created new column with Price Buckets:  =IF(Discounted Price < 200, "<₹200",
     IF(Discounted Price <= 500, "₹200–₹500", ">₹500"))
     - Pivot Table: Rows: Price Bucket, Values: Product Name → Count
-  Relationship Between Average Rating and Discount %
    - Option A: Scatter Chart
  X-axis: Discount %
  Y-axis: Average Rating
     - Option B: Line Chart using Discount Buckets
     - Grouped discount % into ranges (0–10%, 11–20%, etc.)
     - Pivot Table: Rows = Discount Bucket, Values = Average Rating
-  Products with Fewer Than 1,000 Reviews
    - Filtered Rating Count < 1000
    - Used COUNT or Excel status bar
-  Categories with the Highest Discounts
    - Pivot Table:Rows: Category
   Values: Discount % → Max
- Top 5 Products by Combined Score (Rating + Review Volume)
    - Created calculated column: = Average Rating + (Rating Count / 1000)
     - Sorted in descending order
     - Selected top 5 products
   ![Screenshot (93)](https://github.com/user-attachments/assets/912633bf-1b82-46b3-89b0-d84db80bb97f)


![Screenshot (71)](https://github.com/user-attachments/assets/75f69859-d7fd-4cda-b76b-96b406151b89)


