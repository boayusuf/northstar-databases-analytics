# NorthStar Urban Mobility and Logistics

Databases and Analytics coursework for module CP60056E, University of West London (2025-26).

## Case study

NorthStar is a fictional UK urban mobility and logistics group whose operational data is fragmented across multiple systems. Four executives disagree on the cause of rising service failure, cost, and customer dissatisfaction. The analysis in this repo uses the data to resolve that disagreement and to propose a hybrid relational + NoSQL architecture.

## Contents

### Notebooks

| File | Language | Section of assignment |
|------|----------|-----------------------|
| `01_python_cleaning_and_analysis.ipynb` | Python | Python data processing (20 marks) |
| `02_r_sql_analytics.ipynb` | R | SQL in R + R analytics (30 marks) |
| `03_mongodb_and_optimisation.ipynb` | Python / PyMongo | MongoDB development + query optimisation (30 marks) |

Each notebook loads the raw CSVs directly from this repository via `raw.githubusercontent.com`, so they are fully reproducible with a single "Run all".

### Data

Nine raw CSVs under the repo root plus a data dictionary:

- `customers.csv`, `drivers.csv`, `vehicles.csv`, `hubs.csv` — master data
- `orders.csv`, `deliveries.csv` — operational transactions
- `incidents.csv`, `complaints.csv` — exception and case records
- `app_events.csv` — semi-structured mobile platform events
- `data_dictionary.csv` — field definitions

## How to run

### Python and MongoDB notebooks

Open in Google Colab, Runtime → Run all. The MongoDB notebook connects to a MongoDB Atlas free-tier cluster using PyMongo.

### R notebook

Open in Google Colab with an R runtime (Runtime → Change runtime type → R), then Run all.

## Key results

- Delivery failure rate varies from 9% to 20% across hubs
- Central zone has the highest failure rate (19%) and the lowest net margin per order
- Customers of failed deliveries rate the service 1.23 points lower on a 1-5 scale (t-test, p < 10^-32)
- A multiple linear regression model predicts customer rating with test-set R^2 = 0.45
- MongoDB compound and multikey indexes reduce document scans by 99%+ on realistic ops queries

Yusuf Shakir  
Student ID: 33114323
