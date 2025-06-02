# Snowflake Usage Dashboard

A personal project to analyze and visualize Snowflake usage metrics, helping to understand query performance, warehouse utilization, storage patterns, and credits consumption.

Built with Snowflake, Python, and Streamlit.

---

## Project Goals

* Gain hands-on experience with Snowflake query performance and optimization techniques.
* Explore Snowflake's ACCOUNT\_USAGE and INFORMATION\_SCHEMA views.
* Build internal tooling to make Snowflake usage insights accessible.
* Visualize metrics interactively for better decision-making.
* Learn best practices for Snowflake access, Python integration, and Streamlit dashboards.
* (Optional) Implement CI/CD with GitHub Actions for code quality checks.

---

## Dashboard Modules

| Module                    | Description                                                     | Key Visuals                         |
| ------------------------- | --------------------------------------------------------------- | ----------------------------------- |
| Warehouse Usage   | Monitor warehouse activity, credits usage, and load patterns    | Line charts, bar charts, heatmaps   |
| Query Performance | Analyze query execution times, top users, and bottlenecks       | Tables, bar charts, pie charts      |
| Storage Usage     | Track storage by database/schema, table sizes, and trends       | Bar charts, line charts, pie charts |
| Credits Overview  | (Optional) See how credits are consumed across users/warehouses | Bar charts, line charts             |

---

## Project Architecture

```
Snowflake ACCOUNT_USAGE & INFORMATION_SCHEMA Views
        │
        ▼
Python Query Layer (Snowflake Connector)
        │
        ▼
Streamlit App (Interactive Dashboards)
        │
        ▼
(Optional) GitHub CI/CD Pipeline (Linting & Tests)
```

---

## Tech Stack

| Layer               | Tools/Technologies             |
| ------------------- | ------------------------------ |
| Data Source         | Snowflake ACCOUNT\_USAGE views |
| Backend/Querying    | Python, Snowflake Connector    |
| Visualization Layer | Streamlit, Plotly, Pandas      |
| Version Control     | GitHub                         |
| (Optional) CI/CD    | GitHub Actions                 |

---

## Project Structure

```
snowflake-usage-dashboard/
├── app.py                     # Streamlit app
├── snowflake_query.py         # Query logic
├── requirements.txt           # Python dependencies
├── README.md                  # Project documentation
├── .gitignore                 # Ignore files
└── .github/workflows/ci.yml   # (Optional) GitHub Actions CI
```

---

## Getting Started

1️. Clone this repo

```bash
git clone https://github.com/ecslps18/snowflake-usage-dashboard.git
cd snowflake-usage-dashboard
```

2️. Install dependencies

```bash
pip install -r requirements.txt
```

3️. Configure Snowflake connection

* Update `snowflake_query.py` with your Snowflake credentials:

  ```python
  user = 'YOUR_USERNAME'
  password = 'YOUR_PASSWORD'
  account = 'YOUR_ACCOUNT'
  warehouse = 'YOUR_WAREHOUSE'
  role = 'YOUR_ROLE'
  ```

4️. Run the Streamlit app

```bash
streamlit run app.py
```

---

## CI/CD (Optional)

* Set up GitHub Actions for:

  * Linting (e.g., with `flake8`)
  * Basic test execution
  * Future deployment pipelines

---

## Resources

* [Snowflake ACCOUNT\_USAGE Documentation](https://docs.snowflake.com/en/sql-reference/account-usage.html)
* [Streamlit Documentation](https://docs.streamlit.io)
* [Snowflake Python Connector](https://docs.snowflake.com/en/developer-guide/python-connector/python-connector)
