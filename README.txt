# NorthStar Urban Mobility and Logistics

Databases and Analytics assignment, module CP60056E, University of West London.
Yusuf Shakir  
Student ID: 33114323

## Case study

NorthStar is a UK urban mobility and logistics group. Its operational data is fragmented across multiple systems and four executives disagree on the cause of rising service failure, cost, and customer dissatisfaction. The analysis in this repo uses the data to see who's right.

## Notebooks

| File | Language |
|------|----------|
| `01_python_cleaning_and_analysis.ipynb` | Python |
| `02_r_sql_analytics.ipynb` | R |
| `03_mongodb_and_optimisation.ipynb` | Python / PyMongo |

Each notebook loads the CSVs directly from this repo, so they run end to end with one "Run all".

## Data

Nine CSVs plus a data dictionary:

- `customers.csv`, `drivers.csv`, `vehicles.csv`, `hubs.csv`
- `orders.csv`, `deliveries.csv`
- `incidents.csv`, `complaints.csv`
- `app_events.csv`
- `data_dictionary.csv`

## How to run

**Python and MongoDB notebooks:** open in Google Colab, Runtime > Run all. The MongoDB notebook uses a MongoDB Atlas free-tier cluster.

**R notebook:** open in Google Colab, Runtime > Change runtime type > R, then Run all.
