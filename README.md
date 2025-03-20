Global-Ad-Performance-Dashboard

Overview
This project provides a **Global Ad Performance Dashboard** using **Flask, SQLite, and Matplotlib**. It simulates fetching ad performance data, storing it in an SQLite database, and visualizing clicks per campaign.

## Features
- Uses **Flask** to create a REST API endpoint
- Stores ad performance data in **SQLite**
- Fetches data and visualizes clicks per campaign using **Matplotlib & Seaborn**
- Compatible with **Google Colab**

## Setup Instructions

### 1. Install Required Libraries
Run the following command in Google Colab:
```python
!pip install flask pandas matplotlib seaborn
```

### 2. Run the Python Script
Execute the provided Python code in **Google Colab**. It will:
- Create a **SQLite database** (`ad_performance.db`)
- Insert **mock ad data**
- Generate an **API endpoint** at `/api/ad-performance`
- Produce an **output image (`ad_performance.png`)** showing ad clicks per campaign

### 3. View API Data
Once the Flask app is running, you can access the ad performance data by making a GET request:
```python
import requests
response = requests.get('http://127.0.0.1:5000/api/ad-performance')
print(response.json())
```

### 4. View Visualization
The output image `ad_performance.png` will be generated and displayed in Google Colab.

## Example Output
The generated **bar chart** visualizes clicks per campaign, similar to this:
```
+------------+----------+---------+-------------+--------+-------+
| Campaign   | Source   | Medium  | Impressions | Clicks | Cost  |
+------------+----------+---------+-------------+--------+-------+
| Campaign A | Google   | CPC     | 10000       | 500    | 200.5 |
| Campaign B | Facebook | CPC     | 15000       | 800    | 350.75|
| Campaign C | Twitter  | Organic | 5000        | 300    | 100.25|
+------------+----------+---------+-------------+--------+-------+
```

## Notes
- This version **simulates** Google Analytics data.
- To integrate **real Google Analytics data**, use the `google-analytics-data` API with authentication.

## Author
S DSAHANA A

## License
MIT License
