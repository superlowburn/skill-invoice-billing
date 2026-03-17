# Invoice & Billing Skill

A free agent skill for generating professional invoices, calculating totals, and drafting payment reminders.

## Install

```bash
npx skills add automadic/skill-invoice-billing
```

## What It Does

- Generate complete invoices from plain English conversation
- Calculate subtotals, tax, discounts, and late fees
- Draft payment reminders (friendly → firm → final notice)
- Track invoice status in markdown tables

## Usage

```
use invoice-billing skill to create an invoice:
from: [your name/company]
to: [client name/company]
work: [description of work and rates]
net 30, 8.5% tax
```

```
use invoice-billing skill to write a payment reminder for INV-042, $3,200, 12 days overdue
```

## Premium Version

The free version handles invoice generation and reminders. The **premium version** adds Stripe payment link generation, QuickBooks/Xero sync, automated reminder sequences, recurring billing, and revenue reporting dashboards.

**[Get the premium skill at automadic.ai](https://automadic.ai)** — $14/mo

## License

MIT
