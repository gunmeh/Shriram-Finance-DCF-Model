# Shriram-Finance-DCF-Model# Shriram Finance — Equity DCF Valuation Model

An independently built 3-scenario Equity DCF valuation model for **Shriram Finance Limited (NSE: SHRIRAMFIN)**, India's largest retail NBFC by AUM.

Built from scratch in Python using primary research — Annual Report, quarterly earnings, CARE rating rationale, and live market data.

---

## Why Shriram Finance?

Shriram Finance is a single-business NBFC focused on vehicle and MSME lending — making it an ideal candidate for a standalone Equity DCF. For financial companies, PAT (Profit After Tax) is used as the cash flow proxy rather than Free Cash Flow, since debt is their core raw material, not a financing choice.

---

## What the Model Does

- Fetches live market price and share data via `yfinance`
- Strips one-time exceptional items from reported PAT to isolate clean recurring earnings
- Projects PAT across **Bear, Base, and Bull scenarios** over a 5-year horizon
- Calculates Terminal Value using the Gordon Growth Model
- Discounts all cash flows using a **CAPM-derived cost of equity** (G-Sec RFR + Beta × Damodaran India ERP)
- Adjusts for **MUFG Bank's ₹39,618 Cr FDI** — including 47.11 Cr share dilution and capital inflow impact
- Outputs a probability-weighted intrinsic value per share with verdict vs. market price

---

## Key Research Adjustments Made

| Item | Detail |
|------|--------|
| Clean PAT | Stripped ₹1,489 Cr exceptional gain (SHFL divestiture) from FY25 reported PAT of ₹9,761 Cr |
| Share Dilution | Modelled MUFG's 47.11 Cr new share issuance — largest FDI in Indian financial sector history |
| Cost of Equity | Reduced to 14.5% (Base) post CARE AAA upgrade following MUFG deal |
| Growth Rate | Anchored to actual Q3 FY26 AUM growth of 14.63% and NIM compression data |

---

## Installation
```bash
pip install yfinance tabulate
python dcf_shriram_finance.py
```

---

## Skills Demonstrated

- Equity DCF modelling (PAT-based, financial company standard)
- Exceptional item identification and adjustment
- Corporate action modelling (dilution, capital inflow)
- CAPM cost of equity derivation
- Scenario analysis (Bear / Base / Bull)
- Python — `yfinance`, `tabulate`, financial logic

---

## Disclaimer

This model is built for educational and learning purposes only. It does not constitute investment advice.
