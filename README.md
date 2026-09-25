# Krishi Hedge

Krishi Hedge is a smart agricultural price-risk platform designed to help farmers, traders, and agri-business stakeholders make better decisions in volatile commodity markets. The platform combines market intelligence, price forecasting, and hedging guidance into a unified digital experience.

This repository contains the main monorepo for the Krishi Hedge platform, including the web dashboard, PWA, admin dashboard, and the AI/ML forecasting service.

## Overview

Agricultural commodities like soybean, mustard, groundnut, and sunflower are highly sensitive to price volatility. Krishi Hedge addresses this challenge by offering:

- Real-time market data monitoring
- AI-powered price prediction and forecasting
- Hedging and risk-management recommendations
- Farmer-friendly dashboards and decision support tools
- Multi-platform access through web and mobile experiences

## Key Features

- Real-time agricultural commodity price tracking
- Forecasting for short- and medium-term price movement
- Hedging strategy suggestions for risk mitigation
- Insights for farmers, traders, and cooperative stakeholders
- Responsive dashboard for desktop and mobile access
- Admin monitoring interface for business and operations workflows
- Python-based ML service for predictive analytics

## Tech Stack

### Frontend
- Next.js
- React
- TypeScript
- Tailwind CSS

### Backend / Services
- Node.js / pnpm workspace monorepo
- Python FastAPI for ML service
- REST APIs for market and prediction endpoints

### Machine Learning
- Python-based forecasting pipeline
- Pandas, NumPy, and FastAPI stack
- Data-driven price models for commodity trend analysis

## Repository Structure

```text
Krishi-Hedge/
├── root/
│   ├── apps/
│   │   ├── admin-web/       # Admin dashboard
│   │   ├── pwa/             # Progressive Web App
│   │   └── web/             # Public / user-facing web app
│   ├── services/
│   │   └── ml/              # Python forecasting service
│   ├── scripts/             # Startup scripts
│   ├── package.json         # Monorepo scripts
│   ├── pnpm-workspace.yaml
│   └── package-lock.json
├── legacy-site/             # Archived or previous site version
├── START.ps1                # Windows quick-start launcher
├── IMPLEMENTATION_SUMMARY.md
├── NCDEX_SCALE_DATA_DOCUMENTATION.md
├── REAL_TIME_DATA_GUIDE.md
├── login.page
├── login_signup_readme
├── README.md
└── .gitignore
```

## Project Architecture

The platform is organized as a monorepo with separate application packages and a dedicated machine learning service:

- `root/apps/web` — main user-facing web application
- `root/apps/pwa` — mobile-friendly PWA experience
- `root/apps/admin-web` — administration and insight dashboard
- `root/services/ml` — prediction service and market analytics logic
- `root/scripts` — scripts to launch the ecosystem

## Getting Started

### Prerequisites

- Node.js >= 20
- pnpm
- Python 3.10+
- A terminal environment supporting PowerShell or Bash

### Install dependencies

```bash
cd root
pnpm install
```

### Run the apps

Use the workspace scripts:

```bash
cd root
pnpm dev:web
pnpm dev:pwa
pnpm dev:admin-web
```

Or start all development apps together:

```bash
cd root
pnpm dev:all
```

### Start the ML service

```bash
cd root/services/ml
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt
python main.py
```

The ML service is designed to expose forecasting endpoints and analytics used by the platform.

## Quick Start Script

A Windows PowerShell launcher is included for quick startup:

```powershell
./START.ps1
```

This script starts the ML service and PWA in separate terminal sessions, making it easy to test the platform locally.

## Documentation

The repository includes supporting documents for implementation and domain-specific data flow:

- `IMPLEMENTATION_SUMMARY.md` — project implementation notes
- `REAL_TIME_DATA_GUIDE.md` — real-time data and platform guidance
- `NCDEX_SCALE_DATA_DOCUMENTATION.md` — NCDEX scale and data documentation

## License

This project currently includes repository files under the project’s existing codebase structure. Please check the repository for the appropriate license or usage terms before production deployment or redistribution.

## Status

This repository is actively structured as a multi-app agricultural hedging platform with a forecast engine and supporting tooling for farm and market risk management.

## Contact

For questions or collaboration inquiries, please reach out through the repository owner or project maintainer.

---

Built for agricultural market intelligence and price-risk management.
