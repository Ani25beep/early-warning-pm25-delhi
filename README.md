# Early-warning indicators for extreme PM2.5 events in Delhi

This project investigates whether short-term statistical properties of daily PM2.5 concentrations in Delhi show systematic changes before extreme air-pollution events.

The goal is to explore interpretable early-warning indicators using a research-style, event-centred time-series analysis rather than black-box prediction models.

---

## Motivation

Extreme air-pollution episodes pose serious public-health risks.  
While it is common to detect extreme days after they occur, an operationally more useful question is:

Can short-term statistical signals be observed before extreme pollution events?

This project studies this question using simple and interpretable indicators that are widely used in early-warning research in climate, ecology and complex systems.

---

## Data

Daily aggregated PM2.5 concentration data for Delhi derived from sub-daily air-quality measurements.

The dataset is obtained from a publicly available air-quality dataset on Kaggle and is not included in this repository.

---

## Methodology

The analysis consists of the following main steps:

1. Construction of a continuous daily PM2.5 time series.
2. Definition of extreme pollution events using a 95th percentile threshold.
3. Computation of rolling statistical indicators:
   - rolling variance
   - rolling lag-1 autocorrelation
   - rolling skewness
4. Event-centred alignment of indicator values for the days preceding each extreme event.
5. Comparison with randomly selected non-extreme control days.
6. Statistical evaluation using two-sample t-tests and effect size (Cohen’s d).
7. Visualisation of mean trajectories and uncertainty bands.

---

## Early-warning indicators

The following indicators are analysed:

- **Rolling variance** – measures short-term variability.
- **Rolling lag-1 autocorrelation** – indicates persistence and potential critical slowing down.
- **Rolling skewness** – captures changes in distributional asymmetry.

All indicators are computed using fixed rolling windows.

---

## Key findings

- Rolling variance shows a clear and statistically significant increase prior to extreme PM2.5 events.
- Autocorrelation displays an increasing trend before extreme days, consistent with reduced recovery from short-term fluctuations.
- Skewness exhibits weaker but noticeable changes.
- Random control days remain comparatively stable, indicating that the observed patterns are not due to chance.

---

## Limitations

- The indicators are descriptive and do not imply causality.
- Results depend on the chosen rolling window length and threshold definition.
- The number of extreme events is limited, which affects statistical power.
- PM2.5 dynamics are influenced by meteorological and policy factors not explicitly modelled here.

---

## Possible extensions

- Apply the same pipeline to other cities or pollutants.
- Investigate sensitivity to different window sizes and thresholds.
- Combine early-warning indicators with predictive models for short-term risk forecasting.

---

## Repository contents

- `early-warning-pm25.ipynb` – complete analysis notebook

---

## Author

Mayank Kochar
