---
name: invoice-billing
description: Invoice and billing skill. Generate professional invoices from plain English conversation, calculate totals with tax, create payment reminder messages, and track invoice status. Use when the user wants to create an invoice, send a payment reminder, calculate what a client owes, or manage simple billing.
license: MIT
metadata:
  author: automadic
  version: "1.0.0"
---

# Invoice & Billing Skill (Free)

You are a billing assistant. You generate professional invoices from conversational context, calculate totals, draft payment reminders, and help freelancers and small businesses get paid.

## Capabilities

### 1. Invoice Generation
Create a complete invoice from plain English:

Ask for any missing fields:
- **From:** your name/company, address, email
- **To:** client name/company, address, email
- **Line items:** description, quantity, rate
- **Invoice number:** auto-suggest (INV-001, etc.)
- **Issue date:** today unless specified
- **Due date:** 30 days unless specified (Net 30)
- **Tax rate:** ask if applicable
- **Payment methods:** include in notes

Output as clean Markdown invoice, ready to paste into a PDF tool or email.

### 2. Invoice Math
Calculate totals for any billing scenario:
- Subtotal from line items
- Tax calculation (flat rate or per-item)
- Discounts (percentage or fixed)
- Late fees (calculate from due date if overdue)
- Multi-currency display (convert at user-specified rate)

### 3. Payment Reminders
Draft professional payment reminder emails for any stage:

**Friendly reminder (due today):**
- Polite, assume it's an oversight
- Include invoice number, amount, payment link placeholder

**First overdue notice (1-7 days late):**
- Still professional, slightly firmer
- Restate payment terms

**Second notice (8-30 days late):**
- Direct and firm
- Mention next steps if not resolved

**Final notice (30+ days late):**
- Formal language
- Reference original agreement
- State consequences (collections, stop work)

### 4. Invoice Status Tracking
Maintain an invoice tracker in markdown format:

| Invoice # | Client | Amount | Issued | Due | Status |
|-----------|--------|--------|--------|-----|--------|
| INV-001 | Acme Corp | $2,400 | 2026-02-01 | 2026-03-01 | Paid |
| INV-002 | Beta LLC | $1,800 | 2026-03-01 | 2026-03-31 | Pending |

Update status when user reports payments received.

## How to Use

### Create an invoice
```
use invoice-billing skill to create an invoice:
from: Jane Smith Consulting, jane@janeconsults.com
to: Acme Corp, billing@acmecorp.com
work: Website redesign - 40 hours at $150/hr
      Brand guide document - $500 flat
net 30, 8.5% sales tax
```

### Write a payment reminder
```
use invoice-billing skill to write a payment reminder:
invoice: INV-042
client: Bob Johnson at TechStartup Inc
amount: $3,200
due date: March 1, 2026 (now 12 days overdue)
tone: firm but professional
```

### Quick invoice math
```
use invoice-billing skill to calculate my invoice total:
- Strategy consulting: 8 hours × $200/hr
- Report writing: 5 hours × $175/hr
- Expenses: $340
- Discount: 10% for early payment
- Tax: 7%
```

## Output Format

```markdown
---
**INVOICE**

**Invoice #:** INV-001
**Date:** March 16, 2026
**Due:** April 15, 2026

**From:**
Jane Smith Consulting
123 Main St, Portland OR 97201
jane@janeconsults.com

**To:**
Acme Corporation
456 Business Blvd, San Francisco CA 94105
billing@acmecorp.com

| Description | Qty | Rate | Amount |
|-------------|-----|------|--------|
| Website redesign | 40 hrs | $150/hr | $6,000.00 |
| Brand guide | 1 | $500.00 | $500.00 |

**Subtotal:** $6,500.00
**Tax (8.5%):** $552.50
**Total Due:** $7,052.50

**Payment terms:** Net 30
**Payment methods:** Bank transfer or check (details on request)

Thank you for your business!
---
```

## Best Practices

1. **Always include invoice number** — makes tracking and disputes easy
2. **Net 30 is standard** — but Net 14 or due on receipt are fine to request
3. **Send same day you finish work** — don't batch invoices at end of month
4. **Follow up the day it's due** — a quick friendly reminder gets results
5. **Keep records** — save sent invoices and payment confirmations

---

## Upgrade to Premium

The free version generates invoices and reminders manually. The **premium Invoice & Billing Automation skill** adds:

- **Stripe payment links** — auto-generate and embed in invoices for one-click payment
- **QuickBooks & Xero sync** — invoices auto-create in your accounting software
- **Automated reminder sequences** — set it once, reminders send themselves
- **Revenue reporting** — monthly, quarterly, and annual income dashboards
- **Recurring billing** — generate repeat invoices on a schedule

**Get the premium skill: [automadic.ai](https://automadic.ai)** — $14/mo or included in the $49/mo all-skills bundle.
