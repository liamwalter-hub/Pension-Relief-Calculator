# Pension Tax Relief Calculator 2025/26

A single-file, self-contained HTML pension tax relief calculator built for **Bespoke Independent Financial Advisers**. No dependencies, no build step — open `bespoke-pension-calculator.html` in any browser.

---

## What it does

The calculator answers the question higher-rate taxpayers most want answered:

> *"If I put £10,000 into my pension, what does it actually cost me?"*

It shows — clearly and at a glance — the difference between what a person **pays in**, what the **government adds**, and what ends up **working in their pension**. It then breaks down the additional relief available through self-assessment for higher and additional rate taxpayers.

---

## Features

### Core calculation
- Enter gross income and desired gross pension contribution
- Instantly shows the three key numbers: what you pay in, government relief, total in pension
- Displays effective cost per £1 contributed (e.g. "60p of each £1")
- Slices contributions across multiple tax bands for accuracy — if a contribution spans both basic and higher rate, each slice is calculated correctly

### Tax rates covered (2025/26)
| Region | Bands |
|--------|-------|
| England, Wales & Northern Ireland | Personal allowance (0%), Basic (20%), Higher (40%), Additional (45%) |
| Scotland | Personal allowance (0%), Starter (19%), Basic (20%), Intermediate (21%), Higher (42%), Advanced (45%), Top (48%) |

### Self-assessment claim card
- Appears only when the user's income puts them in a higher/additional rate band
- Shows the exact amount they can claim back via self-assessment
- Provides three clear steps on how to make the claim

### Annual allowance checker
- Standard allowance: £60,000
- MPAA (Money Purchase Annual Allowance): £10,000 — toggled on if the user has flexibly accessed their pension
- Tapered allowance: automatically calculated when threshold income exceeds £200,000 and adjusted income exceeds £260,000 — reduces by £1 for every £2 over £260,000, minimum £10,000
- Carry forward: users can add unused allowance from 2022/23, 2023/24 and 2024/25
- Progress bar showing allowance used with colour-coded warnings (amber near limit, red if exceeded)

### Smart warnings
- **Personal allowance taper (60% marginal rate):** income between £100,000–£125,140 — notes that pension contributions can restore the personal allowance
- **Tapered annual allowance:** flags when both threshold income and adjusted income thresholds are breached
- **MPAA:** shown when the toggle is active
- **Contribution exceeds earnings:** relief is capped at 100% of UK earnings
- **Annual allowance exceeded:** flags the excess amount

### Dynamic headline
The main story panel headline updates automatically based on the user's actual top tax band — e.g. "what it really costs a basic-rate taxpayer" rather than always showing "higher-rate taxpayer".

---

## Inputs

| Field | Description |
|-------|-------------|
| Annual income (gross) | Total taxable income before tax |
| Gross pension contribution | The total gross amount to enter the pension (including relief) |
| Employer contribution | Used only to check annual allowance — does not affect relief calculation |
| Tax region | England/Wales/NI or Scotland |
| Carry forward (2022/23, 2023/24, 2024/25) | Unused annual allowance from prior years |
| MPAA toggle | Applies the £10,000 Money Purchase Annual Allowance |

---

## How pension tax relief works (as explained in the calculator)

1. The user pays the **net amount** into their pension. Their provider claims the 20% basic rate top-up directly from HMRC and adds it to the pot.
2. Every **£800 paid in becomes £1,000** in the pension — automatically, before any higher-rate claim.
3. **Higher and additional rate taxpayers** can claim the extra relief (20% or 25%) via self-assessment or by contacting HMRC.
4. Between **£100,000–£125,140**, pension contributions also restore the personal allowance — saving an extra 20p in the pound on that band.

---

## Branding

The calculator uses the **Bespoke Independent Financial Advisers** brand:
- **Teal** `#1DB5AC` as the primary colour — header, footer, buttons, highlights
- **Lime** `#B5C923` as the accent stripe on header and footer borders
- **Lexend** font (loaded from Google Fonts) at light (300) for body and medium/semibold (500/600) for headings
- White Bespoke logo in the header; circular "b." icon in the footer
- FCA regulatory disclaimer in the footer

All logos are embedded as base64 — the file is fully self-contained and works offline.

---

## Known limitations

- Scottish taxpayers claim additional relief above the basic rate (19%) via self-assessment — the calculator notes this but does not automatically calculate the starter rate adjustment at source
- Employer contributions are used only to check the annual allowance — they are not included in the personal tax relief calculation (relief is only available on personal contributions)
- Carry forward is not available to increase the MPAA — the calculator enforces this when the MPAA toggle is on
- Tapered allowance calculation uses a simplified threshold income figure (gross income minus personal contributions) — complex cases involving salary sacrifice or benefits in kind should be verified with an adviser

---

## Disclaimer

This calculator provides estimates for guidance only and does not constitute financial advice. Bespoke Independent Financial Advisers is authorised and regulated by the Financial Conduct Authority. Always verify with HMRC or a qualified adviser before making financial decisions.

---

## Files

```
bespoke-pension-calculator.html   — Complete self-contained calculator
PENSION-CALCULATOR-README.md      — This file
```
