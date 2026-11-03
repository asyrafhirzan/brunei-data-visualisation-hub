# 3-Week Implementation Roadmap (2-3 hours/day)

## Week 1: Ingestion & Parsing Foundation
- **Milestone 1:** Repository setup, folder scaffolding, and documentation finalized.
- **Milestone 2:** Build the base crawler script (`src/ingest/`) to connect to data.gov.bn and inventory target file URLs.
- **Milestone 3:** Write Tier 1 custom Python parsers for the core cost-of-living datasets (CPI & retail prices).
- **Definition of Done (Week 1):** Running a local script successfully downloads raw files and outputs clean, validated tidy CSVs into `data/processed/`.

## Week 2: Front-End Integration & Flagship Analysis
- **Milestone 4:** Initialize Evidence.dev project structure inside `/site`.
- **Milestone 5:** Connect processed CSV data to Evidence.dev using SQL queries.
- **Milestone 6:** Build the flagship Cost of Living topic page (headline charts, summary cards, data table, methodology notes).
- **Definition of Done (Week 2):** Local preview server runs smoothly, displaying interactive charts driven by tidy data.

## Week 3: Automation & Public Polish
- **Milestone 7:** Configure GitHub Actions workflow (`.github/workflows/pipeline.yml`) to orchestrate daily/weekly ingestion, parsing, and site building.
- **Milestone 8:** Add automated failure notifications (GitHub Issues / email alerts).
- **Milestone 9:** Write a comprehensive, recruiter-friendly `README.md` with architecture notes and live deployment link.
- **Definition of Done (Week 3):** Live site successfully deployed on GitHub Pages via CI/CD, fully documented, and verified.