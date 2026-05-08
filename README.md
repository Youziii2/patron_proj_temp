# Canadian Federal Procurement: Cost-Efficiency and Electoral Cycles

> **Note:** This is a temporary working document for an early-stage research idea, not the final project.

## Overview

This project explores the cost-efficiency of Canadian federal procurement awards, looking at whether contract outcomes vary across departments, contract types (defence, infrastructure, environment, services), and electoral cycles. Lee's work inspires both the approach of measuring firm productivity as a proxy for contract outcome quality and the investigation of its relationship with electoral cycles. Fazekas & Czibik's work inspires the index-based measurement of public procurement project outcomes.

Potential research directions:

- Do procurement awards made closer to federal elections show measurable differences in firm productivity or cost-efficiency?
- Do competition mechanisms (open vs. limited vs. sole-source) predict contract cost-efficiency, and does this vary by department or contract type?

## Key Variables of Interest

**Procurement contract variables**:

- Competition type: whether the contract was awarded through open bidding, limited tendering, or sole-source
- Contract sector/type: categorization of the procurement (e.g., national defence, infrastructure, IT, environmental, professional services).
- Contract value: awarded dollar amount, and any amendments/modifications.
- Awarding department or agency
- Award date and contract period
- Number of bids received / level of competition.

**Firm productivity variables** (potentially sourced from Compustat North America via Wharton):

- Revenue per employee as a labour productivity proxy
- Operating income margin as efficiency proxy
- Total assets and asset turnover
- Firm sector

-> These would be matched to procurement award recipients by firm name or business identifier.

**Electoral cycle variables**:

- Date of the most recent and next federal election
- Days elapsed since / remaining until the next federal election
- Binary indicator for a pre-election window (e.g., within 180 days of election)
- Governing party at time of award (for potential partisan alignment analysis)

## File Structure

### `data/`

> The files below are theorized datasets for a hypothesized study design. They do not yet exist and are described here to outline the intended data structure.

- `00-simulated_data/simulated_data.csv` contains simulated data used to test the analysis pipeline.
- `01-raw_data/proactive_disclosure_contracts.csv` contacts contract-level recrods of procurements. Columns include contract reference code, firm name, department, award timeline, contract value, amendment value (if any), description of contracts, and competition type.
- `01-raw_data/compustat_contractors.csv` contains firms' labor productivity proxy, efficiency proxy, such as firm identifier, revenue, employees, operating income, total assets. Or, contains some measurement of the awards cost-efficiency, as well as the procurement outcome measurement. 
- `01-raw_data/elections_canada_results.csv` contains Federal election results and calendar data, such as election date, riding, candidate, party, votes received, and elected indicator.
- `02-analysis_data/analysis_data.csv` contains cleaned and merged contract–firm–year panel of variables aforementioned. 

### `scripts/`

- `00-simulate_data.R` / `00-simulate_data.py` — Simulate data.
- `01-test_simulated_data.R` — Test simulated data.
- `02-download_data.R` — Download raw data.
- `03-clean_data.R` — Clean and merge data.
- `04-test_analysis_data.R` — Test analysis data.
- `05-exploratory_data_analysis.R` — Exploratory analysis.
- `06-model_data.R` — Model estimation.
- `07-replications.R` — Robustness checks.

### `paper/`

- `paper.qmd` — Quarto manuscript.
- `references.bib` — Bibliography.
- `paper.pdf` — Compiled PDF.

### `other/`

- Supplementary materials: articles, datasheet, flowchart, sketches, notes, LLM usage log.

## Statement on LLM Usage

This project was developed with LLM assistance. Usage is logged in `other/llm_usage/usage.txt`.