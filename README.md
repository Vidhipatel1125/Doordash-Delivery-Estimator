# Doordash-Delivery-Estimator
## Introduction
In the modern era of on-demand services, food delivery platforms like DoorDash have become an essential part of urban life. Consumers expect fast, reliable, and predictable delivery times, while delivery drivers and restaurants aim to optimize their operations for efficiency and profitability. However, estimating delivery times accurately remains a challenge due to various dynamic factors, including traffic conditions, restaurant preparation times, driver availability, and weather conditions.

This project aims to develop a DoorDash Delivery Estimator, a predictive model designed to estimate delivery times based on multiple real-world factors. By leveraging data-driven techniques such as machine learning and statistical analysis, the system will provide users with more accurate delivery time predictions compared to traditional static estimations. The primary goal is to enhance user experience by reducing uncertainty, improving logistical efficiency for drivers, and helping restaurants manage their workflow more effectively.

The scope of the project includes collecting and analyzing relevant datasets, identifying key influencing variables, selecting appropriate machine learning models, and evaluating their performance. The estimator will take into account key parameters such as order preparation time, distance, traffic conditions, time of day, and historical delivery performance. By implementing this predictive system, the project aims to improve the overall accuracy of delivery time estimations, reducing delays and enhancing customer satisfaction.

This document outlines the methodology, data sources, model selection, implementation details, and performance evaluation criteria used to build the DoorDash Delivery Estimator. The results of this project can provide insights into optimizing delivery networks and offer potential improvements for food delivery platforms.

## Data Description

This table describes the dataset columns and their respective data types.

| Column Name                                    | Data Type   | Description |
|-----------------------------------------------|------------|-------------|
| `market_id`                                   | Integer    | Unique identifier for the market (region) where the order was placed. |
| `created_at`                                  | Timestamp  | Timestamp indicating when the order was created. |
| `actual_delivery_time`                        | Timestamp  | Timestamp indicating when the order was actually delivered. |
| `store_id`                                    | Integer    | Unique identifier for the store fulfilling the order. |
| `store_primary_category`                      | String     | The primary category/type of the store (e.g., restaurant, grocery, etc.). |
| `order_protocol`                              | Integer    | Protocol used for order placement (e.g., API, manual entry, etc.). |
| `total_items`                                 | Integer    | Total number of items in the order. |
| `subtotal`                                    | Float      | Total cost of the order before taxes, fees, and tips (in cents or dollars). |
| `num_distinct_items`                          | Integer    | Number of unique items in the order. |
| `min_item_price`                              | Float      | Price of the cheapest item in the order. |
| `max_item_price`                              | Float      | Price of the most expensive item in the order. |
| `total_onshift_dashers`                       | Integer    | Number of dashers (delivery drivers) currently on shift in the market at the time of the order. |
| `total_busy_dashers`                          | Integer    | Number of dashers currently assigned to deliveries at the time of the order. |
| `total_outstanding_orders`                    | Integer    | Number of active (unfulfilled) orders in the market at the time of the order. |
| `estimated_order_place_duration`              | Float      | Estimated time (in seconds or minutes) for the restaurant to confirm and prepare the order. |
| `estimated_store_to_consumer_driving_duration`| Float      | Estimated driving time (in seconds or minutes) from the store to the customer's location. |
