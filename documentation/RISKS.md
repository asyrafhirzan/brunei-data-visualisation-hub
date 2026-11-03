# Risk Register

| Risk | Likelihood | Impact | Mitigation Strategy | Owner |
| :--- | :--- | :--- | :--- | :--- |
| **Schema Drift:** Government updates column headers or table structures unexpectedly, breaking parsers. | High | High | Implement strict data validation checks in Python parsers; fail gracefully and alert via GitHub Actions. | Developer |
| **Legal / Licensing Uncertainty:** Unclear redistribution rights on data.gov.bn. | Low | Medium | Include prominent disclaimers ("Unofficial mirror/presentation of public data") and proper agency attribution. | Developer |
| **Portal Structure Changes:** The underlying CMS (WordPress) or URL patterns of data.gov.bn change. | Medium | High | Keep crawler logic modular and isolated; scope flagship analysis to a fixed set of known files. | Developer |
| **Scope Creep:** Attempting to ingest too many of the 686 datasets within the 3-week timeline. | High | High | Enforce strict Tier 1 limit (5-8 core datasets) and a generic Tier 2 fallback. | Developer |