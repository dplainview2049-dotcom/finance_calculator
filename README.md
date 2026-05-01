[readme.md](https://github.com/user-attachments/files/27278701/readme.md)
# Personal Finance Calculator

A single-file, client-side web tool for modelling Australian mortgages, tax projections, and property purchase costs. Built for personal use and client-facing broker conversations.

## Features

**Mortgage interest calculator**
- Principal & Interest or Interest Only
- Weekly / fortnightly / monthly payment frequencies
- Automatic minimum repayment calculation
- Compare minimum vs actual payment scenarios
- Split loan support (two independent portions, each P&I or IO)
- Offset account modelling (balance + monthly contribution)
- Redraw tracking across the life of the loan
- Live SVG chart of balance over time with shaded benefit area
- Yearly breakdown table (interest, principal, closing balance, redraw available)

**AU tax projection (2025-26)**
- Stage 3 income tax brackets
- Medicare levy with correct low-income phase-in
- HECS / HELP debt with 2025-26 marginal rates and indexation tracking
- Division 293 tax on high-income super contributions
- 5 / 10 / 20 year milestone cards
- Year-by-year breakdown showing each tax component separately

**Property purchase estimator**
- Stamp duty schedules for all 8 states and territories (NSW, VIC, QLD, WA, SA, TAS, ACT, NT)
- Owner-occupier vs investor treatment where applicable
- First home buyer concessions for established and new builds
- LMI estimate using Helia / QBE-style rate tables
- Total upfront cash requirement
- Final LVR and loan amount (with LMI capitalised)

**Interface**
- Light and dark mode (follows system preference on first load)
- Responsive layout, mobile friendly
- Fully keyboard navigable
- Live recalculation on every input change

## Live demo

Hosted via GitHub Pages at: `https://<your-username>.github.io/<repo-name>/`

## Quick start

No build step. No dependencies. Clone and open:

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
open index.html
```

To deploy to GitHub Pages: Settings → Pages → Source → Deploy from branch → `main` / `/ (root)` → Save.

## Tech

- Single `index.html` file
- Vanilla JavaScript (no frameworks, no build tools)
- Inline CSS with custom properties for theming
- Inline SVG for charts
- System fonts (no external loads)
- No analytics, no tracking, no cookies, no data leaves the browser

Everything runs client-side. Works offline after first load.

## Data sources and rates

All rates current as of **April 2026**.

| Item | Source | Year |
|---|---|---|
| Income tax brackets | ATO — Stage 3 rates | 2025-26 |
| Medicare levy thresholds | ATO | 2025-26 |
| HECS / HELP marginal rates | ATO | 2025-26 (new marginal system) |
| Division 293 threshold | ATO — unchanged since 2017 | 2025-26 |
| Stamp duty schedules | State revenue offices | 2025-26 |
| QLD FHB new build exemption | QRO — effective 1 May 2025 | Current |
| LMI rate bands | Approximated from Helia / QBE published tables | Indicative |

## Limitations

This is a planning tool, not a tax return or loan contract. Known simplifications:

- Tax projection assumes income held flat (no wage growth, no bracket indexation)
- HECS projection ignores future indexation changes and assumes current rates hold
- LMI is indicative only — real premiums vary by lender, insurer, and professional waivers
- NSW stamp duty uses approximated indexed thresholds; Revenue NSW adjusts these annually
- ACT first home buyer exemption applied as a flat cutoff (ignores the income means test)
- Foreign purchaser surcharges (7-9%) not included
- Home Guarantee Scheme, off-the-plan concessions, and pensioner concessions not modelled
- Offset in split-loan mode applies to one nominated portion only

## Disclaimer

Estimates only. Not financial or legal advice. Figures may differ from official calculators and real-world outcomes. Always verify with the relevant state revenue office, the ATO, and a qualified mortgage broker, accountant, or financial adviser before making decisions.

## License

MIT
