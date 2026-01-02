# Long-Term Commodity Price Estimation Using Historical Trends

This repository documents a **validated, engineering-focused analysis** of long-term commodity price estimation using historical data.

The work evaluates whether historical price trends can be used for **future cost planning**, while explicitly measuring **accuracy, uncertainty, and limitations**.

The study focuses on:
- Copper (benchmark case)
- Aluminium (energy- and policy-sensitive case)

This is **not a trading or speculation project**.  
It is intended for **engineering cost estimation, feasibility studies, and scenario planning**.

---

## Objectives

1. Use historical price data to estimate a future known price (2025)
2. Validate the estimate against actual observed prices
3. Quantify error and structural limitations
4. Assess whether long-term extrapolation (2040) is reasonable
5. Document why prediction uncertainty grows over time

---

## Core Methodology

- Data source: London Metal Exchange (LME)
- Frequency: Monthly prices
- Aggregation: Monthly → Annual averages
- Training window: 1990–2010
- Validation year: 2025
- Forecast horizon: 15 years
- Method: Trend-based statistical time-series estimation (non-ML)

Key rule:
> **No data after 2010 was used to estimate 2025**  
This prevents hindsight bias and preserves scientific validity.

---

## Results Summary

### Aluminium (LME)

| Metric | Value |
|------|------|
| Estimated 2025 price | USD 2,058.70 / MT |
| Actual 2025 price | USD 2,536.64 / MT |
| Absolute error | USD 477.94 |
| Relative error | **18.84%** |
| Directional accuracy | Correct (upward trend) |

Key insight:
- Aluminium is **structurally difficult to forecast** due to energy costs, policy shifts, and geopolitical supply risk.

Full technical report: `Aluminium.pdf`

---

### Copper (Reference Comparison)

Copper showed **significantly lower error** over the same validation horizon, demonstrating that:
- Predictability depends on the **commodity’s structural drivers**
- The same method can perform well for one material and poorly for another

Full technical report: `Copper.pdf`

---

## Why the Original “Just Predict the Future” Idea Was Wrong

This project corrected several common misconceptions:

- Historical data does **not** encode future shocks
- Forecast error grows **nonlinearly** with time
- Long-term prices cannot be treated as single точ values
- Validation matters more than the prediction itself
- Commodity prices ≠ currency prices (policy-driven)

The correct mental model is:
> Use history to **bound uncertainty**, not eliminate it.

---

## 2040 Projection: What Is and Is Not Valid

❌ Invalid:
- Single-number prediction for 2040

✅ Valid:
- Scenario ranges with buffers

For aluminium, reasonable 2040 planning ranges:
- Low: USD 1,800–2,200 / MT
- Base: USD 2,400–2,800 / MT
- High: USD 3,200–4,000 / MT

---

## Engineering Use Cases

Appropriate:
- Long-term cost estimation
- Feasibility studies
- Scenario planning
- Risk exposure analysis

Not appropriate:
- Fixed-price procurement
- Trading or speculation
- Guaranteed forecasts
- Financial advice

---

## Key Takeaway

Historical trend analysis is **directionally useful** for long-term engineering planning but must be paired with **uncertainty buffers, scenario thinking, and periodic reassessment**, especially for energy-sensitive commodities like aluminium.

---

## Disclaimer

This work is for **engineering and planning purposes only**.  
It is not investment advice, trading guidance, or a price guarantee.

---

## Repository Structure

