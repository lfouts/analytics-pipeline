# 📊 Live Website Analytics Pipeline

A fully automated data pipeline that pulls website analytics from 
Google Analytics daily, stores them in InfluxDB, and visualises 
them in a live Grafana dashboard.

## 🔴 Live Dashboard
👉 [View Live Dashboard](https://lorenlove.grafana.net/public-dashboards/ea33555320884f6f8679b42354551839)

## 🏗️ Tech Stack

Google Analytics → n8n → InfluxDB → Grafana

| Tool | Purpose |
|------|---------|
| Google Analytics 4 | Source of website traffic data |
| n8n | Scheduled workflow automation |
| InfluxDB | Time-series database |
| Grafana | Data visualisation dashboard |

## ⚙️ How It Works

1. **n8n** runs daily at 9am and calls the GA4 API
2. Data is sanitised and formatted using a JavaScript node
3. Metrics are written to **InfluxDB** using the line protocol
4. **Grafana** reads from InfluxDB and displays live charts

## 📊 Dashboard Panels
- Website Sessions over time
- Page Views over time  
- Total Users (stat panel)
- Visitor Locations (world map)
- Top Cities (bar chart)

## 🔧 Setup
See `workflow.json` to import the n8n workflow into your own instance.
Update the InfluxDB URL, org, bucket and token with your own credentials.
