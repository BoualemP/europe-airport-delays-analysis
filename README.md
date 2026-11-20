# European Airport Delays: Where Arrival ATFM Delays Build Up

Where do arrival ATFM delays build up at European airports, and how do Lisbon, Porto and Faro compare? This notebook analyses 293 airports in 42 countries reported by EUROCONTROL, from January 2014 to October 2026. ATFM (air traffic flow management) delay is the delay imposed on a flight because of a capacity constraint at its destination airport; it is not total flight punctuality. "Europe" here means every airport EUROCONTROL reports, some of them outside geographic Europe. Source: EUROCONTROL Aviation Intelligence Portal. Data © EUROCONTROL. The data is not included in this repository: the notebook downloads it, keeps a local cache and shows the retrieval date.

## Results

| 2025 | ATFM delay min per arrival | Arrivals with ATFM delay | Rank (of 109 airports with 20,000+ arrivals) | Median of 10 traffic peers (min per arrival) |
|---|---|---|---|---|
| Europe (all airports) | 0.867 | 4.5% | – | – |
| Lisbon (LPPT) | 2.826 | 14.4% | 6th | 0.671 |
| Porto (LPPR) | 2.453 | 7.7% | 7th | 0.256 |
| Faro (LPFR) | 0.015 | 0.1% | 88th | 0.061 |

## Key findings

- Traffic in 2025 is almost back to 2019, but ATFM delay per arrival is higher (0.867 against 0.778 minutes). The highest complete year is 2024 (0.907).
- Weather (44.5%) and capacity (32.8%) account for most ATFM delay minutes. The share of minutes coded as ATC capacity rose from 3.2% in 2015 to 21.8% in 2025.
- Lisbon and Porto are among the most affected airports in Europe. In 2025 both are above all 10 of their traffic peers, and they have been above their peer median every year since 2014. Faro has almost no ATFM delay.
- At Lisbon, weather leads from October to April, but in July and August the capacity group holds over 70% of the minutes. Porto's weather delay is concentrated from July to October.

## Methodology

- Download of the 13 yearly delay files, plus the traffic files used for one check, with a local cache, a `REFRESH` switch and the retrieval date.
- Raw data inspection: mixed text encoding, missing values, the 2016 change in the ATFM delay calculation, inconsistent rows and missing airport-days.
- Cleaning, checked against values computed from the raw data.
- Europe-wide trend and seasonality, airport rankings above a traffic threshold, delay causes by reason group, and comparison with traffic peers.

## Tech stack

Python · pandas · matplotlib · requests · Jupyter

## Project structure

```
europe-airport-delays-analysis/
├── europe_airport_delays_analysis.ipynb
├── requirements.txt
└── README.md
```

## Author

**Boualem Pereira**
