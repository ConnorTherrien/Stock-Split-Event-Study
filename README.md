# Corporate Action Event Study: Stock Split Valuation Impacts

Replication of Grinblatt, Masulis, and Titman (1984) analyzing the changing impacts of stock splits across historical and modern market environments.

## Acknowledgments
This quantitative analysis was developed collaboratively alongside my project partners, **Nick Favoriti** and **Nace Weigand**.

## Overview
This repository contains a quantitative event study replicating the foundational methodology of Grinblatt, Masulis, and Titman (1984). A core focus of this project is evaluating how market reactions have evolved by comparing **pre-2000 and post-2000 sub-periods**. 

Today, stock splits are theoretically purely cosmetic—largely due to the advent of fractional share trading and zero-commission retail platforms. This study investigates whether the historical valuation anomalies and market inefficiencies surrounding stock split announcements and ex-dates still persist in a modern market where share price no longer restricts retail access.

## Data & Scope
* **Data Sources:** Center for Research in Security Prices (CRSP) accessed via Wharton Research Data Services (WRDS).
* **Timeframe:** 1970 – 2024
* **Analytical Sub-Periods:** Pre-2000 (1970–1999) vs. Post-2000 (2000–2024) to isolate the impact of modern trading mechanics.
* **Key Variables:** Daily returns, market capitalization, announcement dates (`dclrdt`), and ex-dates (`exdt`).

## Methodology
The analysis utilizes a **Constant Mean Return Model** to evaluate equity performance across both eras.
* **Estimation Window:** Calculated over a 40-day post-event window to establish a baseline expected return.
* **Metric of Interest:** Daily Abnormal Returns (AR) were computed to isolate the specific market reaction attributable to the corporate action, stripping out broader market movements.
* **Data Handling:** Implemented robust preprocessing to handle massive datasets, including merging daily returns with specific event identifiers and adjusting for delisting anomalies.

## Technical Stack
* **Language:** Python
* **Libraries:** `pandas`, `numpy`, `matplotlib`, `wrds` API
* **Environment:** Jupyter Notebook

## Key Takeaways
* **Impact of Fractional Trading:** Observed a major structural shift in the volume of stock splits, noting a significant decline prior to the widespread introduction of fractional share trading, reinforcing the idea that splits serve less of a practical mechanical purpose today.
* **Announcement Abnormal Returns:** Despite the cosmetic nature of modern splits, statistically significant abnormal returns persist in the post-2000 subset in the days leading up to, and up to three days following, a stock split announcement.
* **Ex-Date Market Dynamics (Pre- vs. Post-2000):** Identified a distinct shift in ex-date behavior. Prior to 2000, abnormal returns clustered in the few days before and after the split. Post-2000, abnormal returns are highly concentrated on the exact ex-date.
* **Liquidity & The Signaling Hypothesis:** We attribute the ongoing anomalies in the modern era not to systematic market changes, but rather to strategic corporate actions:
    * *Liquidity Provision:* Splits are still utilized to generate retail liquidity and psychological momentum for high-share-price companies.
    * *Positive Signaling:* Executing a split acts as a strong signal from management indicating a belief that the firm is currently undervalued, strategically utilizing the event to increase market visibility.
