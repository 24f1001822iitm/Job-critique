# 💼 Job Critique

**Job Critique** is a full-stack Data Engineering + Visualization project that automates the ETL of job listing data into Snowflake and delivers beautiful dashboards for insight discovery using Streamlit and Plotly.

It leverages **real-world job data (65,000+ rows)** scraped from **Google Jobs** and other job posting APIs/websites.

---

## 👤 Author

**24f1001822iitm** — Built as part of a Data Engineering project exploring real-world job market trends using Python, Snowflake, and Streamlit.

---

## 🚀 Features

✅ Extracts and loads job data from a CSV file (~65K rows)  
✅ Automatically sets up Snowflake warehouse, database, schema, and tables  
✅ Creates raw and analytical tables in Snowflake  
✅ Interactive dashboards with Plotly & Streamlit  
✅ Modular Python codebase and clean architecture

---

## 🏗️ Architecture

```plaintext
         [65K+ Row CSV File from Google Jobs & APIs]
                       |
                    Extract
                       |
             Load into Snowflake Tables
                       |
     ┌─────────────────┬──────────────────┬──────────────────┐
     │ raw_jobs        │ industry_analysis│ job_posting_trends
     └─────────────────┴──────────────────┴──────────────────┘
                       ↓
            Visualize with Streamlit Dashboard
```

---

## 🛠️ Setup

1. Clone the repo:
   ```bash
   git clone https://github.com/24f1001822iitm/Job-critique.git
   cd Job-critique
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Configure your `.env` file (copy from `.env.example`):
   ```bash
   cp .env.example .env
   ```

4. Run the pipeline:
   ```bash
   python main.py
   ```

---

## 📊 Dashboard

Launch the Streamlit dashboard:
```bash
streamlit run dashboard/app.py
```

---

## 📁 Project Structure

```
Job-critique/
├── dashboard/        # Streamlit + Plotly visualizations
├── load/             # Snowflake data loading logic
├── setup/            # Warehouse, DB, schema setup
├── sql/              # SQL queries and table definitions
├── transform/        # Data transformation scripts
├── utils/            # Helper utilities
├── main.py           # Entry point
├── requirements.txt  # Python dependencies
└── .env.example      # Environment variable template
```

---

## 🔐 Environment Variables

Copy `.env.example` to `.env` and fill in your Snowflake credentials:

```
SNOWFLAKE_USER=your_user
SNOWFLAKE_PASSWORD=your_password
SNOWFLAKE_ACCOUNT=your_account
SNOWFLAKE_WAREHOUSE=your_warehouse
SNOWFLAKE_DATABASE=your_database
SNOWFLAKE_SCHEMA=your_schema
```
