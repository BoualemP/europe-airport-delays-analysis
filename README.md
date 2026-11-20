# European Airport Delays: Where Arrival ATFM Delays Build Up

Analysis of airport arrival ATFM delays at 293 airports in 42 countries reported by EUROCONTROL, from January 2014 to October 2026, with a focus on Lisbon, Porto and Faro. ATFM (air traffic flow management) delay is the delay imposed on a flight because of a capacity constraint at its destination airport; it is not total flight punctuality. In this project, "Europe" and "Europe-wide" mean all airports reported by EUROCONTROL, which include some outside geographic Europe; the 42 countries are listed in section 3.9 of the notebook. Source: EUROCONTROL Aviation Intelligence Portal. Data © EUROCONTROL. Not included in this repository: the notebook downloads it from the source, keeps a local cache and shows the retrieval date.

## Results

| 2025 | ATFM delay min per arrival | Arrivals with ATFM delay | Rank (of 109 airports with 20,000+ arrivals) | Median of 10 traffic peers (min per arrival) |
|---|---|---|---|---|
| Europe (all airports) | 0.867 | 4.5% | – | – |
| Lisbon (LPPT) | 2.826 | 14.4% | 6th | 0.671 |
| Porto (LPPR) | 2.453 | 7.7% | 7th | 0.256 |
| Faro (LPFR) | 0.015 | 0.1% | 88th | 0.061 |

## Key findings

- With almost the same traffic as in 2019, Europe-wide ATFM delay per arrival is higher in 2025 (0.867 against 0.778 minutes); the highest complete year is 2024 (0.907).
- Weather (44.5%) and capacity (32.8%) account for most ATFM delay minutes; the share of ATC capacity grows from 3.2% in 2015 to 21.8% in 2025.
- Lisbon and Porto are among the most affected airports in Europe: in 2025 both are above all 10 of their traffic peers, and they are above the median of their peers in every year since 2014. Faro has almost no ATFM delay.
- At Lisbon, weather is the largest cause from October to April, while in July and August the capacity group holds over 70% of the minutes; Porto's weather delay is concentrated from July to October.

## Methodology

- Download of the 13 yearly delay files (and of the traffic files, used for one check) with a local cache, a `REFRESH` switch and the retrieval date.
- Raw data inspection: mixed text encoding, missing values, the 2016 change in the ATFM delay calculation, inconsistent rows and missing airport-days, ending in a findings and decisions table.
- Cleaning, with checks against values computed from the raw data.
- Europe-wide trend, seasonality (month × year heatmap), airport rankings with a minimum traffic threshold, delay causes by the source's reason groups, and comparison with 10 traffic peers.

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
