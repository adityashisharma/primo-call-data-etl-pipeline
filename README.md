# Call Data ETL Pipeline

This repository provides a scaffold for an **automated ETL pipeline** that:
- Extracts call details from an API (e.g., Primo, Twilio, custom telecom APIs).
- Transforms the data into a clean tabular format.
- Loads the data into a relational database (Azure SQL, PostgreSQL, MySQL).

## ✨ Features
- Nightly automation (via Azure Functions / App Service / Cron).
- Secure secrets handling (use Azure Key Vault or environment variables).
- Extendable to any API by modifying the `fetch_calls()` function.

## ⚙️ Setup
1. Clone this repo  
   ```bash
   git clone https://github.com/YOURNAME/call-etl-pipeline.git
   cd call-etl-pipeline
2. Install dependencies
   ```bash
   pip install -r requirements.txt
3. Create config.json based on config.example.json with your API and DB credentials.
4. Run locally
   ```bash
   python etl_calls.py
5. Deploy to Azure Functions or any scheduler.
