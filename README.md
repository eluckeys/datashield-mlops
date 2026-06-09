# DataShield Fraud Detection — MLOps Project

Building a production-grade fraud detection pipeline for DataShield India.
Following 100 Days of MLOps challenge.

## The Problem
Data science team builds models that work on their laptops but fail
in production due to different package versions, missing configs,
and no automation.

## The Goal
Take fraud detection model from "works on my machine" to fully
reproducible, automated, monitored production system.

## Progress

| Day | Task | What I Learned |
|-----|------|----------------|
| 01 | Python virtual environment | venv = isolated env, pip freeze = snapshot |
| 02 | JupyterLab server | Web server config, 0.0.0.0 vs 127.0.0.1 |

## Project Structure
fraud-detection/
├── day-01-python-venv/    ← venv + requirements.txt
├── day-02-jupyterlab/     ← jupyter config + notes
├── .venv/                 ← virtual environment (not tracked)
├── requirements.txt       ← pinned dependencies
└── README.md              ← this file

## Quick Start

```bash
git clone https://github.com/eluckeys/datashield-mlops.git
cd datashield-mlops/fraud-detection
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## Author
Lucky — Linux Admin → MLOps Engineer
GitHub: @eluckeys
