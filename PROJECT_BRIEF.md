# Project Brief: Brunei Open Data Hub

## Problem Statement
Government open data portals (such as data.gov.bn) provide raw spreadsheets and files, but raw data is rarely accessible to the general public or journalists. Files are siloed, formatted inconsistently, and lack visual context, commentary, or unified trend analysis.

## Target Audience
- **Primary:** The general public in Brunei looking for clear, understandable insights on national metrics (e.g., cost of living, retail prices, inflation).
- **Secondary:** Hiring managers and recruiters looking for evidence of clean data engineering, automated pipeline design, and product execution.

## Goals
1. Automatically ingest public datasets from data.gov.bn without manual intervention.
2. Standardize raw files into clean, validated, tidy tabular formats (CSV/Parquet).
3. Build a modular configuration-driven charting engine using SQL and Markdown.
4. Publish a static, zero-cost data hub via GitHub Pages, updated automatically via GitHub Actions.
5. Deliver a flagship cost-of-living analysis (CPI, subsidised vs. non-subsidised retail prices) alongside a generic dataset explorer.

## Non-Goals
- Achieving 100% coverage of all 686 datasets on the portal (scope is strictly selective).
- Building a real-time streaming pipeline (government data is periodic/annual).
- Storing data in expensive cloud databases (keeping everything static/local build artifacts).

## Success Criteria
- Fully automated CI/CD pipeline that checks for updates, parses files, and rebuilds the site without errors.
- Clean, responsive static site deployed on GitHub Pages with sub-second page loads.
- A well-documented repository that clearly demonstrates end-to-end data engineering craftsmanship.