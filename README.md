# shiny-guide

This repository contains sample data files for Data Science programming exercises and analysis.

## Sample Data Files

The `data/` directory contains three sample datasets that can be used for various Data Science tasks:

### 1. sales_data.csv
A comma-separated values (CSV) file containing sales transaction data for an office supplies store.

**Use cases**: Sales analysis, revenue forecasting, product performance analysis, customer segmentation

**Columns**:
- `date`: Transaction date
- `product_id`: Unique product identifier
- `product_name`: Name of the product
- `category`: Product category (Electronics, Furniture, Stationery, Office Supplies)
- `quantity`: Number of units sold
- `unit_price`: Price per unit
- `revenue`: Total revenue for the transaction
- `customer_id`: Customer identifier

**Sample analyses**:
- Calculate total revenue by category
- Identify best-selling products
- Analyze sales trends over time
- Customer purchase patterns

### 2. customers.json
A JSON file containing customer information and purchase history.

**Use cases**: Customer analytics, demographic analysis, loyalty program analysis, customer lifetime value prediction

**Fields**:
- `customer_id`: Unique customer identifier
- `name`: Customer name
- `email`: Email address
- `age`: Customer age
- `city`, `state`, `country`: Location information
- `registration_date`: Date when customer registered
- `total_purchases`: Number of purchases made
- `lifetime_value`: Total amount spent by customer
- `preferred_category`: Most purchased product category
- `loyalty_tier`: Customer loyalty level (Bronze, Silver, Gold, Platinum)

**Sample analyses**:
- Segment customers by demographics
- Analyze lifetime value by loyalty tier
- Geographic distribution of customers
- Correlation between age and spending patterns

### 3. temperature_readings.csv
A time series CSV file containing hourly temperature, humidity, and pressure readings from multiple sensors.

**Use cases**: Time series analysis, sensor data visualization, environmental monitoring, forecasting, anomaly detection

**Columns**:
- `timestamp`: Date and time of reading
- `sensor_id`: Sensor identifier (S001, S002, S003)
- `location`: Sensor location (Room_A, Room_B, Outdoor)
- `temperature_celsius`: Temperature in degrees Celsius
- `humidity_percent`: Relative humidity percentage
- `pressure_hpa`: Atmospheric pressure in hectopascals

**Sample analyses**:
- Visualize temperature patterns throughout the day
- Compare indoor vs outdoor conditions
- Detect correlations between temperature, humidity, and pressure
- Forecast future readings using time series models
- Identify anomalies or unusual patterns

## Getting Started

You can load these datasets using common Python libraries:

```python
import pandas as pd
import json

# Load CSV files
sales_df = pd.read_csv('data/sales_data.csv')
temperature_df = pd.read_csv('data/temperature_readings.csv')

# Load JSON file
with open('data/customers.json', 'r') as f:
    customers = json.load(f)
# Or with pandas
customers_df = pd.read_json('data/customers.json')
```