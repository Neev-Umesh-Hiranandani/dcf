# Financial-Models

Two unlevered DCF models on Indian large-cap consumer names, built from the annual
reports up. Each opens live in your browser, no download needed, and the assumptions
are editable so you can test them yourself.

Both models are run as **expectations analyses**: rather than arguing a target price,
they solve for the perpetual growth rate the traded price already embeds, and ask
whether that rate is defensible.

**Neev Hiranandani** · [hiranandanineev@gmail.com](mailto:hiranandanineev@gmail.com)

| Model | Valuation date | WACC | Market-implied g | g used here | |
|---|---|---|---|---|---|
| **Asian Paints** (NSE: ASIANPAINT) | 31 Mar 2026 | 11.8% | 10.4% | 2.0% | [Open live ↗](https://1drv.ms/x/c/a5bc101168becf89/IQBnNdUBpvdISZjblS6ic6cSAXRVZ110sLqrxyNZA_f3Nuw?e=NIN7xQ) · [.xlsx](Neev_Umesh_Hiranandani_Asian_Paints_DCF_FINAL.xlsx) |
| **Nestlé India** (NSE: NESTLEIND) | 31 Dec 2018 | 11.0% | 9.3% | 2.0% | [Open live ↗](https://1drv.ms/x/c/a5bc101168becf89/IQDwOT8K0KoaQIz2j6CsQT9sAYGyKSDss8m0xcxoaIzxeIw?e=WILY6r) · [.xlsx](Neev_Umesh_Hiranandani_Nestle_India_DCF_FINAL.xlsx) |

---

## Asian Paints (NSE: ASIANPAINT)

**Intrinsic ₹444.7 vs. traded ₹2,164.5 · WACC 11.82% · terminal g 2.0% · TV is 66% of EV**

Valued at 31 March 2026, ₹ crore, unlevered DCF with a five-year explicit forecast and
a Gordon growth terminal value.

At a 2.0% perpetual growth rate the model values the equity at ₹444.7 per share against
a traded ₹2,164.5. The more useful reading runs the other way: holding WACC at 11.82%,
the traded price solves to a **perpetual growth rate of 10.4%**, sitting only 1.5
percentage points below the discount rate itself. Since terminal value is 66% of
enterprise value, essentially the entire gap between this model and the market lives in
the terminal assumption rather than in the five-year forecast, which tracks consensus
reasonably closely.

**Assumptions**

- **Revenue:** 6.5% CAGR FY26 to FY31, decelerating from 7.0% to 6.0%
- **Margins:** EBITDA held at 19.4%, EBIT easing to 15.8% by FY31
- **Free cash flow:** ₹2,797 cr in FY27 to ₹4,446 cr in FY31, a 12.3% CAGR
- **WACC 11.82%:** 7.11% risk-free (India 10Y), equity beta 0.70, 6.9% market risk premium
- **Cost of debt:** 7.71% pre-tax, 25.17% marginal tax rate under section 115BAA
- **Terminal growth 2.0%**, with the sensitivity grid running 1.0% to 6.0% against WACC
  from 9.82% to 14.82%

**[→ Open the model](https://1drv.ms/x/c/a5bc101168becf89/IQBnNdUBpvdISZjblS6ic6cSAXRVZ110sLqrxyNZA_f3Nuw?e=NIN7xQ)** · [Download .xlsx](Neev_Umesh_Hiranandani_Asian_Paints_DCF_FINAL.xlsx)

---

## Nestlé India (NSE: NESTLEIND)

**Intrinsic ₹2,700.1 vs. traded ₹11,107.0 · WACC 10.97% · terminal g 2.0% · TV is 69% of EV**

Valued at 31 December 2018, ₹ million, unlevered DCF with a five-year explicit forecast.
Share count and price are pre-split, matching the FY2018 annual report.

The traded price at the valuation date solves to a **perpetual growth rate of 9.3%**
against the 2.0% applied here. Terminal value carries 69% of enterprise value, so the
same conclusion holds: the market's valuation of Nestlé India rested almost entirely on
its long-run growth assumption rather than on near-term cash flows.

The equity bridge treats employee benefit and contingency provisions of ₹26,222m as
debt-like, per note 37 of the FY2018 annual report.

**Assumptions**

- **Free cash flow:** ₹16,184m in FY19 to ₹24,846m in FY23, an 11.3% CAGR
- **WACC 10.97%:** 6.73% risk-free, equity beta 0.8482, 5.0% market risk premium
- **Beta** regressed on 60 months of Nestlé India returns against the Nifty 50, Jan 2014
  to Dec 2018
- **Cost of debt:** 8.5% pre-tax, 30% marginal tax rate
- **Terminal growth 2.0%**, sensitised from 0.5% to 3.5% against WACC from 9.47% to 11.97%

**[→ Open the model](https://1drv.ms/x/c/a5bc101168becf89/IQDwOT8K0KoaQIz2j6CsQT9sAYGyKSDss8m0xcxoaIzxeIw?e=WILY6r)** · [Download .xlsx](Neev_Umesh_Hiranandani_Nestle_India_DCF_FINAL.xlsx)

---

## How the models are built

Both follow the same structure: historical statements tied out to the annual report,
forecast P&L, balance sheet and free cash flow, a WACC build with beta regressed from
monthly price data, the DCF itself, a two-way sensitivity grid, and a reconciliation
that backs out the market-implied terminal growth rate.

The Asian Paints file also carries a source tie-out sheet mapping every historical line
to its annual report page, and a decision log recording each judgement call and why it
was made.

Blue cells are hardcoded inputs, grey are formulas, yellow are case selectors. Each
model runs bullish, base and bearish cases from a single selector cell.

Built from annual reports and exchange price data. Estimates are my own. For discussion
purposes, not investment advice.
