# Plato’s Pizza Sales Analysis
<img src="Images/pizza img.webp" width="400" height="225">

## Project Overview
Plato's Pizza, a Greek-inspired pizza restaurant in New Jersey, has been collecting transactional data for the past year. However, they have not leveraged this data to enhance their operations. The primary objective of this analysis is to extract actionable insights from their sales data to optimize business performance.

---

##  Understanding the Data
The dataset contains the following columns:

- `order_details_id` (unique identifier for order details)
- `order_id` (unique identifier for each order)
- `pizza_id` (identifier for different pizzas)
- `quantity` (number of pizzas ordered)
- `order_date` (date of order)
- `order_time` (time of order)
- `unit_price` (price per pizza)
- `total_price` (total price per order)
- `pizza_size` (size of the pizza)
- `pizza_category` (type of pizza)
- `pizza_ingredients` (ingredients used)
- `pizza_name` (name of the pizza)

##  Data Processing
- **Added Derived Columns:**
  - `Weekday`: Extracted from `order_date` using `=TEXT([@[order_date]], “dddd”)`
  - `Time groups`: Categorized `order_time` using VLOOKUP based on predefined time slots
  - `Months`: Extracted from `order_date` using `=TEXT([@[order_date]], “mmmm”)`

##  Analysis & Insights

### **1. What days and times do we tend to be busiest? How can we optimize operations during peak hours**
<img src="Images/orders on week days.png" width="260" height="150"> <img src="Images/Timeframe of orders.png" width="260" height="150">
- **Busiest Day:** Friday (8,106 orders)
- **Busiest Time Slot:** 12 PM - 2 PM (12,754 orders)
- **Analysis:** Friday being the busiest day suggests increased demand on weekends. The highest volume of orders occurring between 12 PM - 2 PM highlights the lunch rush.
- **Recommendation:** Increase staffing and prep during peak hours, optimize promotions for slower days.
  

### **2. How many pizzas are we making during peak periods? How can we expand production capacity accordingly?**
<img src="Images/orders during months.png" width="360" height="200"> 
- **Peak Months:** July (4,392), May (4,328), March (4,261), November (4,266)
- **Total pizzas made in peak months:** 17,247
- **Analysis:** Seasonal trends suggest higher sales in summer and holiday months.
- **Recommendation:** Stock up on ingredients in peak months, offer seasonal promotions during off-season.

### **3. What are our best and worst-selling pizzas? Should we discontinue or modify underperforming pizzas?**
<img src="Images/pizza categories.png" width="360" height="200">
- **Best Seller:** The Classic Deluxe Pizza (2,453 orders), The Barbecue Chicken Pizza (2,432 orders) & The Hawaiian Pizza (2,422 orders)
- **Worst Seller:** The Brie Carre Pizza (490 orders)
- **Analysis:** Some pizza types significantly outperform others, indicating customer preference.
- **Recommendation:** Discontinue or revamp the lowest-selling pizzas and focus marketing efforts on the top performers.

### **4. What's our average order value? How can we introduce upselling strategies to increase order value?** 
- **Average Order Value:** $16.82 (~$17) 
- **Analysis:** Most Customers tend to buy 1-2 pizzas per order. 
- **Recommendation:** Introduce upselling strategies such as meal combos and loyalty card discounts. 

### **5. How well are we utilizing our seating capacity?**
<img src="Images/seating arrangement.png" width="360" height="200">
- **Average Orders per Seating:** 20.7 orders/hour
- **Seats Available:** 60
- **Analysis:** The restaurant has excess seating capacity during most hours.
- **Recommendation:** Consider implementing a reservation system to better manage seating, explore delivery/takeout strategies to maximize revenue.

---

##  Conclusion
This analysis provided actionable insights for Plato’s Pizza to optimize its operations. Key takeaways include:
- **Peak hours and days:** Busiest on Fridays, most orders between 12 PM - 2 PM.
- **High-demand periods:** Peak sales months are May, July, March, and November.
- **Sales trends:** Certain pizzas dominate while others underperform.
- **Revenue insights:** The average customer spends ~$17 per order.
- **Seating utilization:** The restaurant has unused seating capacity, suggesting potential for better management.

###  **Final Recommendations:**
1. Optimize staff scheduling and ingredient stocking based on peak sales trends.
2. Focus marketing on best-selling pizzas and revise the menu for underperforming items.
3. Introduce promotions to increase sales on slow days and during off-peak hours.
4. Implement bundling strategies and upsell techniques to increase order value.
5. Improve seating management, explore reservations, and emphasize takeout/delivery options.

This project demonstrates how businesses can leverage data-driven insights to make informed decisions and drive growth.

