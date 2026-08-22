[FINANCE-README.md](https://github.com/user-attachments/files/31340537/FINANCE-README.md)
# SpendScope — Personal Finance Tracker

A spending tracker that doesn't just show where your money went — it tells you
**exactly what to cut**.

**Live site:** https://DanielTheUNT.github.io/Finance-Tracker/

## What it does

Most budget apps stop at a pie chart. SpendScope runs an analysis pass over your
transactions and returns a concrete action list:

- **Category budget targets** — every category is compared against a
  recommended share of your take-home income (housing 33%, groceries 10%,
  dining out 6%, and so on). Overspending is flagged with the exact dollar
  amount to cut.
- **Biggest line items** — for each over-budget category, it surfaces the
  specific merchants driving the overage, so you know what to change.
- **Delivery-fee detection** — flags DoorDash/UberEats/Grubhub orders and
  totals what ordering delivery cost you versus pickup.
- **Subscription audit** — counts active subscriptions, totals the monthly and
  annualized cost, and lists each one for review.
- **Savings verdict** — compares actual savings against your goal and states
  the monthly shortfall you need to close.

Plus category budget bars, an SVG donut breakdown, and CSV export.

## Usage

1. Enter your monthly take-home income and pick a savings goal.
2. Add transactions (description, category, amount, date).
3. Read the "What to cut — exactly" panel.

Click **Load sample month** to see a full analysis immediately with example data.

## Tech

Single-file vanilla JavaScript application — no build step, no dependencies, no
backend. Transactions persist in `localStorage`, so data stays in the browser
and is never uploaded anywhere. Charts are hand-rendered SVG.

## Budget targets

Category targets are derived from 50/30/20-style budgeting guidance, broken out
into concrete spending categories. They're starting points, not financial
advice — adjust the `TARGETS` object in the source to fit your situation.

## Run locally

Download `index.html` and open it in any browser. That's the whole app.
