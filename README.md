# Stock-Split-Event-Study
Replication of Grinblatt, Masulis, and Titman (1984) analyzing stock split impacts on modern data

## Overview
This repository contains a quantitative event study replicating the foundational methodology of Grinblatt, Masulis, and Titman (1984). The objective of this project is to analyze market efficiency and the short-term valuation impacts surrounding stock split announcements and ex-dates using modern historical data.

## Data & Scope
* **Data Sources:** Center for Research in Security Prices (CRSP) accessed via Wharton Research Data Services (WRDS).
* **Timeframe:** 1970 – 2024
* **Key Variables:** Daily returns, market capitalization, announcement dates (`dclrdt`), and ex-dates (`exdt`).

## Methodology
The analysis utilizes a **Constant Mean Return Model** to evaluate equity performance.
* **Estimation Window:** Calculated over a 40-day post-event window to establish a baseline expected return.
* **Metric of Interest:** Daily Abnormal Returns (AR) were computed to isolate the specific market reaction attributable to the corporate action, stripping out broader market movements.
* **Data Handling:** Implemented robust preprocessing to handle massive datasets, including merging daily returns with specific event identifiers and adjusting for delisting anomalies.

## Technical Stack
* **Language:** Python
* **Libraries:** `pandas`, `numpy`, `matplotlib`, `wrds` API
* **Environment:** Jupyter Notebook

## Key Takeaways
*(Note: Enter 1-2 bullet points here summarizing your final financial conclusion, e.g., "The data confirmed a statistically significant positive abnormal return in the days immediately following a split announcement, aligning with the signaling hypothesis.")*
