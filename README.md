# 🌦 Daily Weather Email Automation (n8n)

This project automates weather updates using OpenWeatherMap and n8n. Every morning at 8 AM, it checks the weather in Islamabad:

- ☀️ If it's not raining → sends an email
- 🌧 If it *is* raining → logs the details in a Google Sheet

## 📂 Files

- `workflow.json` – Full n8n workflow (importable)
- `rain-log-sample.csv` – Example of logged rain data
- `sample-email.png` – Example of weather email

## 🔗 🌧 Sample Rain Log
Since no rainy day has been recorded yet, here's a sample log file to show how data is stored when it rains.

📊 [View Live Log Sheet](https://docs.google.com/spreadsheets/d/1DjasYNq8zgI2YEhvVxgGhtjOtmb9JrbCChQdREirGBk/edit?gid=0#gid=0)
📄 [View `rain-log-sample.csv`](./rain-log-sample.csv)

📝 Note:  
Sample data was added for demonstration. The actual workflow will log real rainy days automatically when conditions match.

## 🛠 Setup

1. Import the JSON file into n8n
2. Replace the placeholder "appid": "PASTE_YOUR_API_KEY_HERE" with your actual OpenWeatherMap API key.
3. In the Gmail node, update the "sendTo" field from some@email.com to your real recipient email.
4. Set your Google Sheets credentials
5. Trigger manually or let it run daily via Cron

## 🔮 Future Ideas

- Telegram alerts
- Multi-city reports
- Rain frequency dashboard
