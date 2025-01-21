![swiggy-logo](https://github.com/user-attachments/assets/556d8e5f-798b-4188-a3d9-27cf9ee231b3)


# **Swiggy Data Analysis Project**

## **Overview**
This project analyzes a Swiggy dataset to uncover key insights related to customers, orders, restaurants, delivery partners, and profit generation. Using Excel, the dataset was cleaned, formatted, and analyzed to create meaningful reports and visualizations. Pivot tables and charts were used to answer critical industry-specific questions, which can help optimize Swiggy’s operations.

---

## **Dataset Description**
The project is based on a dataset consisting of four tables:
1. **Restaurant Table:**
   - `restaurant_id`: Unique identifier for restaurants.
   - `restaurant_name`: Name of the restaurant.
   - `city`: City where the restaurant is located.
   - `ratings`: Average rating of the restaurant.
   - `total_reviews`: Total number of reviews the restaurant has received.

2. **Orders Table:**
   - `delivery_address`: Address where the order was delivered.
   - `expected_delivery_date`: The expected date of delivery.
   - `expected_delivery_time`: The expected time of delivery.
   - `delivery_partner_id`: Identifier for the delivery partner.
   - `profit`: Profit generated from the order.

3. **Delivery Partner Table:**
   - `partner_id`: Unique identifier for delivery partners.
   - `partner_name`: Name of the delivery partner.
   - `city`: City where the delivery partner operates.

4. **Customer Table:**
   - `customer_id`: Unique identifier for customers.
   - `customer_name`: Name of the customer.
   - `address`: Address of the customer.
   - `city`: City of the customer.
   - `email`: Email address of the customer.
   - `phone_number`: Phone number of the customer.

---

## **Data Cleaning and Preparation**
Before performing the analysis, the dataset was cleaned and formatted to ensure accurate results:
1. **Trimming and Removing Duplicates:**
   - Used Excel's **TRIM()** function to remove extra spaces from text fields (e.g., restaurant names, city names).
   - Removed duplicate rows from the dataset where necessary.

2. **Formatting Columns:**
   - Ensured proper data types:
     - Dates in `expected_delivery_date` were formatted as **Date**.
     - Times in `expected_delivery_time` were formatted as **Time**.
     - Numeric fields like `ratings`, `profit`, and `total_reviews` were formatted as **Number** or **Currency**.
   - Extracted the **hour** from `expected_delivery_time` for time-based analysis using Excel’s **HOUR()** function.

3. **Merging Tables:**
   - Used **VLOOKUP** to combine necessary columns from different tables, such as adding `city` from the restaurant table to the orders table for city-based analysis.

4. **Handling Missing Data:**
   - Checked for and handled missing or incomplete data:
     - Removed rows with missing `restaurant_id` or `customer_id`.
     - Replaced missing numeric values (e.g., profit) with 0.

5. **Derived Fields:**
   - Created additional columns:
     - **Delivery Hour**: Extracted from `expected_delivery_time` for time analysis.
     - **Order Month**: Extracted from `expected_delivery_date` to analyze monthly trends.

---

## **Key Questions Addressed**
Here are the business questions addressed and the methods used to find insights:

1. **Number of Customers and Orders by City**
   - **Method**: Grouped orders and unique customers by city using pivot tables.
   - **Visualization**: Bar chart showing customer and order count by city.

2. **Best Restaurants Based on Ratings**
   - **Method**: Filtered and sorted restaurants by ratings and total reviews.
   - **Visualization**: Horizontal bar chart of top-rated restaurants.

3. **Restaurants with the Most Orders and Profit**
   - **Method**: Aggregated total orders and profits per restaurant.
   - **Visualization**: Combined bar chart comparing the number of orders and profits by restaurant.

4. **Delivery Partners with the Most Deliveries and Profit (City-Wise)**
   - **Method**: Grouped delivery partners by city, then calculated the total deliveries and profits for each partner.
   - **Visualization**: Stacked bar chart showing deliveries and profit by city and delivery partner.

5. **Dishes with the Most Orders and Percentage of Profit They Generate**
   - **Method**: Created a custom column for dishes (if dish-level data is present) and calculated the total orders and percentage contribution to profit.
   - **Visualization**: Pie chart showing profit contribution by top dishes.

6. **Top Late Deliveries (Delivery Partner-Wise)**
   - **Method**: Filtered orders with the largest difference between expected and actual delivery times, grouped by delivery partner.
   - **Visualization**: List of late deliveries ranked by lateness.

7. **Number of Orders by Month (with City Slicer)**
   - **Method**: Extracted the month from delivery dates and grouped orders by month, with a slicer for cities.
   - **Visualization**: Line chart showing monthly trends, with a slicer for cities.

---

## **Visualizations**
The following charts were created to support the findings:
- **Bar Charts**:
  - Number of customers and orders by city.
  - Best restaurants by ratings.
  - Restaurants with the most orders and profit.
- **Stacked Bar Chart**:
  - Delivery partner performance (deliveries and profit) by city.
- **Pie Chart**:
  - Percentage of profit generated by dishes.
- **Line Chart**:
  - Monthly order trends with a city slicer.
- **List/Ranking Table**:
  - Top late deliveries by delivery partner.

---

## **Findings**
Here are the major insights derived from the analysis:
1. **Customer and Order Distribution:**
   - City "Delhi" has the highest number of customers and orders, making it a key focus area for Swiggy.
   
2. **Top Restaurants:**
   - Restaurant "Biryani House" is the highest-rated restaurant, with an average rating of 4.8 and over 500 reviews.
   - Restaurant "Biryani House" generates the most profit and receives the most orders.

3. **Delivery Partner Performance:**
   - Delivery Partner "Dhanuk Garg" completes the most deliveries in City "Delhi".
   - Delivery Partner "Dhanuk Garg" generates the highest profit.

4. **Dishes and Profit:**
   - Dish "Chole Bhature" is the most ordered dish and contributes 10.34% of the total profit.

5. **Monthly Order Trends:**
   - Peak orders occur in **August**.

---

## **How to Use the Files**
1. **Dataset (`Swiggy_Dataset.xlsx`)**:
   - Contains the original data used for analysis.
2. **Analysis File (`Swiggy_Analysis.xlsx`)**:
   - Includes cleaned data, pivot tables, and all visualizations created for the analysis.
3. **Charts**:
   - Charts are embedded in the `Swiggy_Analysis.xlsx` file for easy access and interpretation.

---

## **How to Reproduce the Analysis**
1. Open the `Swiggy_Analysis.xlsx` file in Excel.
2. Navigate to the pivot table sheets to explore the data:
   - Use slicers to filter data by city, month, or delivery partner.
   - Modify pivot tables as needed for further insights.
3. Review the charts in the visualization sheets.

---

## **Future Scope**
- Add real-time data and perform analysis in Python or Power BI.
- Use machine learning to predict order demand and late deliveries.
- Perform deeper dish-level analysis if dish data is available.

---

## **Dashboard**
![swiggy1](https://github.com/user-attachments/assets/1f7df885-75c2-4d4b-be10-3b17a281a90e)
![swiggy2](https://github.com/user-attachments/assets/828ae2c4-5fb1-4f7b-b0d3-ccba2a25e9a7)


## **Contributors**
- https://github.com/ankit-biz – Data Analysis and Visualization.

---
