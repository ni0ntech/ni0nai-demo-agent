# Security Scraper 🕷️🧠

A modular, Selenium-powered web scraping framework built with Scrapy + undetected-chromedriver to collect infosec articles from sites like The Hacker News, BleepingComputer, and DarkReading. Designed for automation, ML analysis, and AWS Lambda deployment.

---

## 🚀 Features

- ✅ JavaScript-rendered scraping using undetected Chrome
- ✅ Modular spider architecture (1 module per source)
- ✅ JSON output for data pipelines or ML ingestion
- ✅ Dockerfile for AWS Lambda deployment
- ✅ Cloud-ready: plug into S3, DynamoDB, or RDS
- ✅ Easily schedulable via `run_all.py` or CloudWatch Events

---

## 🧱 Project Structure

```
security_scraper/
├── scrapy.cfg
├── run_all.py
├── test_spider.py
├── output/
├── webcrawler/
│   ├── __init__.py
│   ├── settings.py
│   └── spiders/
│       ├── __init__.py
│       ├── base_spider.py
│       ├── thehackernews_spider.py
│       ├── bleepingcomputer_spider.py
│       └── darkreading_spider.py
```

---

## 🐍 Local Testing

```bash
# Run individual spider and write to output/test.json
python test_spider.py

# Run all spiders and write to output/{name}.json
python run_all.py
```

---

## ☁️ Lambda Deployment

```bash
# Build container
docker build -t security-scraper .

# Push to AWS ECR and deploy to Lambda (see AWS docs)
```

The `lambda_scrapy_docker.zip` contains:
- Dockerfile
- Lambda-compatible `entrypoint.py`

---

## 🧪 Future Plans

- [ ] DynamoDB integration
- [ ] Threat enrichment (MITRE mapping, IOCs, etc.)
- [ ] NLP classification / topic modeling
- [ ] CLI tool or API endpoint

---

## 💣 Author

Built by [Joshua Rubio](https://ni0ntech.com) – InfoSec vet, SOC mentor, and certified cyber war machine.

---

## 📜 License

MIT License
