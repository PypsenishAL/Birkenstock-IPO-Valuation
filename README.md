# Birkenstock IPO Valuation

An Excel valuation of Birkenstock Holding plc (NYSE: BIRK) as of September 30, 2023. The project compares the actual IPO offer price of **$46.00 per share** with a discounted cash flow (DCF) valuation and a comparable company analysis (trading comps).

**Base-case DCF: $38.85 per share, 15.5% below the offer price.** The median multiples of the four core peers imply prices of **$22.23 to $47.67**, depending on the multiple. The forward EV/EBITDA estimate is slightly above the offer price.

<img width="2883" height="1513" alt="image" src="https://github.com/user-attachments/assets/5a09167c-39cc-4fd8-8db9-af838a3cc1f2" />


## Discounted Cash Flow

The model forecasts free cash flow to the firm (FCFF) for FY2024E–FY2030E from a FY2023E base. Revenue growth slows from 25% to 6%, while gross margin declines from 60% to 57%. Forecast EBIT and net property, plant and equipment use inputs from the case. Operating working capital is forecast from inventory, receivables and payables turnover and other operating balances as a share of sales. CapEx is estimated from the change in net PP&E plus depreciation.

`FCFF = EBIT × (1 − tax rate) + D&A − CapEx − ΔOperating NWC`

| DCF input or output | Base case |
| --- | ---: |
| Operating tax rate | 25.00% |
| Cost of equity (CAPM, peer-based beta) | 9.40% |
| After-tax cost of debt (assumed BB credit spread) | 5.47% |
| Weighted average cost of capital (WACC) | 8.65% |
| Terminal growth (2030E ROIC × average reinvestment rate for 2028E–2030E) | 3.16% |
| Present value of forecast FCFF | €2,019.0m |
| Present value of terminal value | €6,064.3m |
| Enterprise value | €8,083.4m |
| Equity value, after €1,546m net debt | €6,537.4m |
| Implied price, using 177m pre-IPO shares and 1.052 USD/EUR | **$38.85** |

<img width="2782" height="1452" alt="image" src="https://github.com/user-attachments/assets/d18fea4c-adb2-465b-9586-2d4c15ca91f7" />

### Sensitivity to WACC and terminal growth

Terminal value accounts for **75% of enterprise value**. In the appendix sensitivity grid, moving WACC and terminal growth by up to 100 basis points each around the unrounded base case yields **$26.88–$64.42 per share**. Each scenario discounts both the forecast cash flows and terminal value at its own WACC.

<img width="2773" height="1436" alt="image" src="https://github.com/user-attachments/assets/161a3cf1-91dc-44a0-8c15-92547ea57cec" />


## Comparable Company Analysis

The core peer set consists of **Crocs, Deckers, Dr. Martens and On Holding**. The selection considers product mix, brand positioning, growth, scale and leverage. The team also tested an eight-company set that adds Skechers, Steve Madden, Cooper and Sonova, and a three-company set that excludes On Holding.

| Multiple | Core peers (4) | Expanded set (8) | Core peers excluding On (3) |
| --- | ---: | ---: | ---: |
| EV/Sales | $22.23 | $8.40 | $10.32 |
| EV/EBITDA | $42.10 | $21.33 | $17.23 |
| Forward EV/EBITDA | $47.67 | $25.36 | $20.88 |

Each figure is the implied price in USD per share from the median peer multiple. The multiple is applied to Birkenstock’s FY2023E revenue or EBITDA, or to FY2024E EBITDA for the forward multiple. Net debt is then deducted from enterprise value to arrive at equity value. The drop from **$47.67 to $20.88** on forward EV/EBITDA when On Holding is excluded shows how much peer selection matters in a small sample.

<img width="2741" height="1404" alt="image" src="https://github.com/user-attachments/assets/677ced5e-1d1d-4569-92cf-7d2dad847408" />

## Files and model walkthrough

| File | Contents |
| --- | --- |
| [Birkenstock_Valuation_Model.xlsx](Birkenstock_Valuation_Model.xlsx) | Excel model with financial inputs, FCFF, WACC, DCF scenarios and trading comps |
| [Birkenstock_Valuation_Presentation.pdf](Birkenstock_Valuation_Presentation.pdf) | Project findings, valuation football field and sensitivity appendix |

1. Open `Historical & Projections` for the FY2023E base and forecast inputs, then `WACC` for the discount rate.
2. Follow `DCF part 1 (FCFF)` to `DCF part 2` for annual cash flows, terminal value, the enterprise-to-equity bridge and implied price. The base case is in column D.
3. Open `Market Approach` for peer multiples and price estimates. Rows 53–60 show the four- and eight-company sets. The section beginning at row 86 shows the impact of excluding On Holding.

<!--
Repository setup: save this file at the root. Rename the workbook and presentation to match the links above, or update the links. Place the PNGs in assets/ and move each image line outside its comment once its PNG exists.
-->

## Contribution

This was a team project

## Sources

- Company disclosure context comes from Birkenstock’s [Form F-1](https://www.sec.gov/Archives/edgar/data/1977102/0001193125-23-233488-index.htm). The [subsequent SEC filing](https://www.sec.gov/Archives/edgar/data/1977102/000095017024022619/R17.htm) confirms the offer price. The valuation uses the case’s pre-IPO share count and capital structure.
