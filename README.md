# EMI & Loan Calculator

Interactive EMI calculator and home-loan prepayment planner — a single-file HTML app that runs entirely in your browser, even offline.

**Live app:** https://devtripathix.github.io/EMI-and-Loan-Calculator/

## What it does

Enter your loan (amount, interest rate, tenure, first EMI month) and build a prepayment plan — the dashboard recalculates everything live:

- **EMI calculation** — with sliders and quick-pick chips (₹50 L – ₹1.5 Cr)
- **Reduce tenure vs reduce EMI** — compare both ways a lender can apply prepayments, side by side
- **Prepayment options**
  - Extra amount with every EMI (starting any month)
  - Year-end lumpsum prepayment
  - One-time lumpsums at any month (bonus, maturity, asset sale)
  - Annual EMI step-up — +5%, +10% or custom
- **Live results** — payoff date, months saved, interest saved, total interest, extra paid
- **Charts** — outstanding balance, cumulative interest with the savings gap, and a yearly interest / principal / prepayment split; responsive with hover tooltips
- **Scenario lab** — every strategy on its own vs all combined, with one-click *Apply*
- **Amortization schedule** — yearly or monthly view, CSV export for Excel

## The math

EMI = P·r·(1+r)ⁿ / ((1+r)ⁿ − 1) on monthly rest, rounded to the nearest rupee.

- **Reduce tenure** — the EMI stays fixed; every prepayment shortens the loan (maximum interest savings).
- **Reduce EMI** — the EMI is recalculated after each prepayment to hold the original close date; ongoing extras can still close the loan earlier.

Amounts use Indian formatting (lakh / crore) and ₹ currency. Processing fees, insurance and other charges are not modelled.

## Run it

Open `index.html` in any modern browser — no install, no server, no internet required (fonts load from Google Fonts when online and fall back gracefully offline).

## Files

| File | Purpose |
|---|---|
| `index.html` | The entire app — HTML + CSS + JS in one file |
