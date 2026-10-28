# Costco Financial Analytics — Starter Kit

One real retailer, three fiscal years, and a clear business question. **Start here after Supply Chain!**

## Contents
- `data/costco_2026_10k_sample.csv`: **actual** Costco figures, USD **millions**, transcribed from 2026 10-K; 2024–2026 income statements, 2025–2026 balance sheets. Missing balance sheet fields for 2024 are deliberately blank, not zero.
- `notebooks/01_costco_intro.ipynb`: beginner-friendly Python notebook. Works offline using bundled CSV. Includes optional live SEC JSON download.
- `requirements.txt`: dependencies.

## How to start
1. Extract the ZIP fully (keep folders together).
2. Have Python 3.10+ installed, open a terminal inside `Costco_Analytics_Starter`.
3. Run `python -m pip install -r requirements.txt`.
4. Run `jupyter notebook notebooks/01_costco_intro.ipynb` (or open it directly in VS Code with the Python/Jupyter extensions).
5. Click **Run All**. Offline sections 0–5 will work with no web connection; 6–7 need a real email in the SEC User-Agent and network access.

## Business objective
Analyze revenue and operating margins, investigate 2026 inventory turnover and payables, then scale up to more fiscal years and retail competitors. Later: forecast operational improvements and assess hypothetical CapEx using **incremental** cash flows, WACC and NPV.

## Sources
Costco FY2026 10-K (filed October 7, 2026):
https://www.sec.gov/Archives/edgar/data/909832/000090983226000093/cost-20260830.htm

SEC public Company Facts API docs:
https://www.sec.gov/search-filings/edgar-application-programming-interfaces

Costco Company Facts endpoint:
https://data.sec.gov/api/xbrl/companyfacts/CIK0000909832.json

SEC asks automated clients to identify themselves and avoid excessive requests. See https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data

## Caveats
- Fiscal years are Costco's 52-week years ended near August, *not* calendar years.
- DPO based on merchandise costs is a proxy, not the usual actual-credit-purchases denominator.
- The tiny CSV is only a learning sample, not yet a sufficiently large dataset for predictive machine learning.
- The later SEC API pipeline will require careful concept harmonization, fiscal-year-end mapping, filing-period checks, and handling repeated comparative facts.
