<h1 align="center">Hello World MLOps</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker">
  <img src="https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white" alt="Flask">
  <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white" alt="GitHub Actions">
  <img src="https://img.shields.io/badge/MLflow-0194E2?style=for-the-badge&logo=mlflow&logoColor=white" alt="MLflow">
</p>

<p align="center">
  <em>End-to-end MLOps pipeline: model training, CI/CD, Docker & Flask API</em>
</p>

---

## Overview

This repository demonstrates a tiny reproducible MLOps flow:
1. Train a small model (`train.py`) — writes `artifacts/model.pkl` and `artifacts/metrics.json`
2. Run predictions from the command line with `run_model.py --input "[5.1,3.5,1.4,0.2]"`
3. Start a minimal Flask app with `python src/app.py` that serves `/predict`
4. Build a Docker image with `docker build -t hello-mlops .`
5. CI trains the model and uploads artifacts

## Tech Stack

- **Python** — Core language
- **Flask** — API server
- **Docker** — Containerization
- **GitHub Actions** — CI/CD pipeline
- **MLflow** — Experiment tracking

## Getting Started

```bash
git clone https://github.com/skyson-ai/hello-world-mlops.git
cd hello-world-mlops
pip install -r requirements.txt

# Train model
python train.py

# Run predictions
python run_model.py --input "[5.1,3.5,1.4,0.2]"

# Start API
python src/app.py
```

## Docker

```bash
docker build -t hello-mlops .
docker run -p 5000:5000 hello-mlops
```

## Author

**MICHEE CEPHAS** — [GitHub](https://github.com/skyson-ai)
