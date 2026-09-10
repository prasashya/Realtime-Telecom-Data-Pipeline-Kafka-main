# Telecom Data Pipeline Dashboard ☁️

A beautiful Streamlit dashboard for visualizing telecom streaming data from a Kafka pipeline.

## 🎯 Features

- 📊 **Real-time Metrics**: Total calls, revenue, average duration
- 🥧 **Interactive Charts**: Pie charts, bar charts, histograms
- 📈 **Time Series**: Call activity over time
- 📋 **Data Table**: Recent call records
- 🎨 **Premium UI**: Dark theme with glassmorphism design

## 🚀 Deployment Options

### Option 1: Demo Mode (No Database Required)
The app works out of the box with realistic demo data!

[![Deploy to Streamlit](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://share.streamlit.io)

### Option 2: Connect to Supabase (Live Data)

1. Create a free account at [Supabase](https://supabase.com)
2. Create the `telecom_data` table:
```sql
CREATE TABLE telecom_data (
    caller_name VARCHAR(256),
    receiver_name VARCHAR(256),
    caller_id VARCHAR(20),
    receiver_id VARCHAR(20),
    start_datetime TIMESTAMP,
    end_datetime TIMESTAMP,
    call_duration INTEGER,
    network_provider VARCHAR(50),
    total_amount DECIMAL(5,2)
);
```

3. Add secrets in Streamlit Cloud:
```toml
SUPABASE_HOST = "db.xxxxx.supabase.co"
SUPABASE_PORT = "5432"
SUPABASE_DB = "postgres"
SUPABASE_USER = "postgres"
SUPABASE_PASSWORD = "your-password"
```

## 📂 Files

- `streamlit_app.py` - Main dashboard application
- `requirements.txt` - Python dependencies

## 🏗️ Architecture

```
Kafka Producer → Kafka Broker → Consumer → PostgreSQL/Supabase
                                                  ↓
                                          Streamlit Dashboard
```

## 👤 Author

**Prasashya Anshul** - Data Engineer
- GitHub: [@prasashya](https://github.com/prasashya)
- Email: prasashyaanshul@gmail.com

---
*Part of the Kafka-Spark-Redshift Streaming Pipeline Project*
