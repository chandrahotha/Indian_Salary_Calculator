# Salary Studio

**Offline salary, payroll and income-tax calculator for India.**

Salary Studio turns an annual CTC into a full picture of your pay: monthly take-home, gross salary, PF, ESI, professional tax, income tax under both regimes, bonus timing, gratuity, employer cost and a draft payslip. Everything runs inside one `index.html` file. There is no install, no build step, no account and no network connection.

**Live site:** https://chandrahotha.github.io/Indian_Salary_Calculator/

- **One file, fully offline** — open `index.html` in a modern browser and start.
- **Real tax engine** — FY2024-25 through FY2027-28, old and new regimes, rebate, surcharge, cess and marginal relief.
- **India-wide** — central tax, PF and ESI rules, plus a State/UT picker for professional tax. No state is assumed.
- **16 focused modules** — from CTC structure and take-home to offers, payslips, gratuity and freelance income.
- **Live and precise** — every number updates as you type, with steppers, draggable sliders and source notes.
- **Light and dark themes** — a colourful glass interface that stays readable in both.

---

## Quick start

### Option 1: open the file directly

1. Download or clone this repository.
2. Double-click `index.html`, or drag it into Chrome, Edge, Firefox or Safari.

That is the whole setup. The calculator does not need a web server.

### Option 2: clone with Git

```bash
git clone https://github.com/chandrahotha/Indian_Salary_Calculator.git
cd Indian_Salary_Calculator
```

Then open `index.html`.

### Optional local server

If your browser restricts local files, run a small static server from the project folder:

```bash
python -m http.server 8000
```

Open `http://localhost:8000`.

---

## Your first calculation

1. **Enter your annual CTC** on the opening screen. Type a number, drag the CTC slider, or tap a preset such as `₹18L`.
2. **Set the basic percentage.** 40% is the default. Most Indian employers use 40–50%, and this choice affects PF, gratuity and HRA.
3. **Choose Metro or Non-metro.** Metro means Delhi, Mumbai, Kolkata or Chennai, where the HRA benchmark is 50% of Basic + DA instead of 40%.
4. **Select your State / UT.** Professional tax is the one input that changes by state, so Salary Studio does not assume one. Every state and union territory is listed.
5. Check the **live preview** on the right (or below, on mobile). It shows monthly in-hand, annual tax, the proposed salary split and the effective tax rate before you commit.
6. Press **Calculate my take-home**. Salary Studio builds a conventional structure and opens the dashboard.
7. Fine-tune anything in **Salary Structure**. The dashboard, tax pages, timeline and payslip all recalculate from the same inputs.

If you already know every salary component, choose **Enter components manually** instead of starting from CTC.

> The opening screen deliberately starts empty. No sample salary is loaded, so the first figure you see is yours.

---

## The workspace

| Area | What it does |
| --- | --- |
| **Top bar** | Switch financial year, toggle Old/New regime, change light/dark theme, open the command palette. Your state is chosen on the first screen and can be changed later in PF, ESI & Prof. Tax. |
| **Left sidebar** | All 16 modules, grouped into Overview, Your salary, Planning, Documents and More tools. On mobile it opens from the menu button. |
| **Main view** | The active module. Inputs save instantly and the page recalculates as you go. |
| **Live summary rail** | Desktop: a persistent panel with monthly in-hand, annual tax, CTC, the winning regime and quick actions. |
| **Bottom dock** | Mobile and tablet: the same in-hand figure plus tabs for Dashboard, Structure, Income Tax, Timeline and More. Tap the in-hand area to open the full summary. |
| **Scenario sheet** | Save, load, duplicate, import or export alternative salary setups. |

### Defaults

- Financial year: **FY2026-27**
- Tax regime: **New**
- State for professional tax: **chosen by you on the first screen** — no state is assumed
- Theme: **Light**, unless you previously chose dark

Change the year or regime in the top bar. Change your state later in **PF, ESI & Prof. Tax**.

---

## Modules

### Overview

| Module | Use it for |
| --- | --- |
| **Dashboard** | The one-screen answer: monthly in-hand, annual tax, deductions, salary mix and a donut breakdown. |
| **Take-Home Pay** | Gross-to-net walkthrough with every deduction and employer contribution explained. |
| **Income Tax** | Slab-by-slab tax computation for the active regime, with rebate and marginal relief. |
| **Old vs New Regime** | Independent side-by-side tax calculations, plus 80C, 80D, home-loan interest, other deductions and HRA exemption inputs. |

### Your salary

| Module | Use it for |
| --- | --- |
| **Salary Structure** | Build CTC from Basic, DA, HRA, allowances, bonus, employer PF, NPS and insurance. Reconcile the entered CTC against the modeled one. |
| **PF, ESI & Prof. Tax** | Employee/employer PF, VPF, EPS split, ESI eligibility and the state professional-tax table. |
| **Bonus & Variable Pay** | Set annual bonus or variable pay, one or two payment months (January, March or any month), a custom split, the tax caused by the bonus, and the take-home in each payment month. |

### Planning

| Module | Use it for |
| --- | --- |
| **Hike & Job Offers** | Compare current and new CTC on absolute and percentage terms. Save each offer as a scenario for a full take-home comparison. |
| **12-Month Timeline** | Monthly gross, bonus, TDS and net projection with a bar chart and table. |

### Documents

| Module | Use it for |
| --- | --- |
| **Payslip** | A draft monthly payslip with earnings, deductions, net pay and employer contributions. Print it directly. |
| **Settings & Rules** | Rule sources, confidence badges, FY/regime/profile settings, Income-tax Act 2025 section mapping, limitations and test tools. |

### More tools

| Module | Use it for |
| --- | --- |
| **CTC, Gross & Net** | Plain-language definitions of the three numbers people mix up. |
| **Employer Cost** | Annual CTC plus employer ESI, with PF and NPS shown as costs already inside CTC. |
| **Gratuity & Leave** | Gratuity eligibility and exemption, plus leave-encashment exemption under 10(10AA). |
| **Freelance Income** | Section 44ADA presumptive taxation for professional receipts. |
| **Formulas & Glossary** | The exact formulas and a short glossary for checking a payroll figure. |

---

## Precision controls

- **Type directly** into any amount field. Values are validated and clamped to sensible minimums and maximums.
- **Use the steppers** beside a field for small, exact adjustments. The step size matches the field (for example ₹500 for salary components, 5% for the basic percentage).
- **Drag the sliders** for CTC and basic percentage on the opening screen, and other ranges inside modules. The coloured fill tracks the value.
- **Watch the live preview** before confirming. Nothing is hidden until you press a button.
- **Open “Source & assumptions”** panels to see where a rule comes from and how confident the figure is.
- **Hover or tap the dashboard donut and legend** to isolate a slice and read its amount and share.

### Confidence badges

Every rule area is tagged:

- **Official** — taken from the law or an official source.
- **Adjustable** — depends on your employer, state or policy; confirm locally.
- **Estimate** — could not be independently confirmed; treat it as approximate.

State professional-tax tables and employer admin charges are the main adjustable or estimate areas. See **Settings & Rules** for the current list.

---

## Bonuses and variable pay

Bonus is treated as annual pay, not as part of your regular monthly salary. Open **Bonus & Variable Pay** and set:

1. **Annual bonus / variable pay** — the total for the year.
2. **Instalments** — one payment or two.
3. **Payment month(s)** — January is the default because many companies pay a year-end bonus with the January salary. March, December or any other month works too.
4. **First payment share** — only for two payments. 50% splits equally; use 60, 70 or another share if the first instalment is larger.

The screen then shows the exact amount and take-home for each instalment, the extra tax the bonus causes, and the regular monthly TDS. The **12-Month Timeline** places the bonus in the chosen months and includes the bonus tax withheld in that month. The **Payslip** module shows a regular month and links the bonus months back to the timeline.

A bonus does not reduce your regular monthly take-home: regular salary is taxed first, and the bonus is priced on top.

If your entered annual CTC **already includes** the bonus, add the bonus and then open **Salary Structure** and press **Re-split from CTC**. The bonus is kept, while Basic, HRA and allowances are rebalanced so the modeled CTC matches your offered CTC.

---

## Scenarios

Scenarios let you keep several salary setups without losing your current one. Open **Scenarios** from the sidebar, the summary rail or the command palette.

- **Save** the current inputs under a name.
- **Load** a saved scenario to restore those inputs.
- **Duplicate** or **delete** scenarios.
- **Export** one scenario as JSON, or **import** a JSON file on another machine.
- Scenarios are stored in your browser's `localStorage` under `indiaSalaryCalc.scenarios.v1`. They are not uploaded or synced.

A useful pattern for a job offer: save your current job as “Current”, change the structure to the new offer, save it as “Offer A”, then compare the dashboard in-hand figures.

---

## Printing and exports

- **Print report** (top bar, sidebar, Dashboard summary or mobile summary) opens the browser print dialog with a clean, report-only layout. Sidebars, buttons and background effects are removed.
- **Print payslip** in the Payslip module opens the same print-safe report, generated from the current salary inputs.
- **Export CSV** in **Settings & Rules** downloads a one-page salary summary: CTC, gross, taxable income, annual tax, net annual and net monthly.
- **Export JSON** in the Scenarios sheet downloads the selected scenario with a schema version and export date.

Printing uses your browser's own print-to-PDF option if you need a PDF.

---

## Keyboard shortcuts

| Shortcut | Action |
| --- | --- |
| `Ctrl+K` / `Cmd+K` | Open or close the command palette |
| `↑` / `↓` | Move through palette results |
| `Enter` | Open the highlighted module or run the highlighted action |
| `Esc` | Close the palette, summary sheet or mobile sidebar |

The palette searches every module and the common actions: toggle theme, open scenarios, print, export CSV and run the calculation tests.

---

## Tax rules and data

Salary Studio ships with four financial years:

- **FY2024-25** (AY2025-26) — carried forward, marked unverified
- **FY2025-26** (AY2026-27)
- **FY2026-27** (Tax Year 2026-27) — the default
- **FY2027-28** (Tax Year 2027-28) — placeholder, marked unverified

FY2027-28 exists so the year picker keeps working past 31 March 2027, but its slabs are carried forward from FY2026-27 because no Finance Act 2027 has been published to this build. It is flagged unverified everywhere in the app. Replace its figures with the enacted rates before relying on them.

If the app is ever asked for a year it does not hold rates for (a stale saved scenario, a hand-edited import), it falls back to the **newest** year it has and shows a red banner saying so. It never silently borrows an older year's rates.

FY2026-27 uses the Income-tax Act, 2025, which applies from 1 April 2026. The Act is a consolidation and renumbering; the rates and limits are unchanged from FY2025-26. For example, the 87A rebate is now section 156, 80C is section 123 and 80D is section 126. The app keeps the familiar section names in its explanations and shows the mapping in **Settings & Rules**.

The engine covers:

- New-regime and old-regime slabs, standard deduction, 87A rebate, surcharge, health and education cess, and marginal relief.
- Employee and employer PF, EPS, VPF, ESI, and state professional tax.
- HRA exemption, 80C, 80D, home-loan interest and other old-regime deductions.
- Employer NPS under 80CCD(2).
- Bonus timing, monthly TDS, 12-month net schedule and a draft payslip.
- Gratuity under the Payment of Gratuity Act and leave encashment under 10(10AA).
- Section 44ADA presumptive income for freelancers.
- CTC, gross, net and employer-cost reconciliation.

Rule sources, verification dates and caveats are shown in the app. Rates were last checked on **28 October 2026** for FY2026-27.

---

## Testing

Salary Studio includes its own calculation test suite. It runs entirely in the browser.

1. Open **Settings & Rules**.
2. Under **Tools & verification**, choose **Run calculation tests**.
3. The sheet reports each test as passed or failed, with expected and actual values.

There are **27 tests**, covering slab tax, rebate and marginal relief, PF and the wage ceiling, fixed-PF overrides, ESI, professional tax, HRA, employer contributions, TDS reconciliation, bonus, hikes, scenarios, CSV and import validation, print styles, edge cases and network isolation. A healthy build shows **27/27 passed**.

Nothing about the test run is uploaded.

---

## Privacy

- All calculations happen in your browser.
- The app makes **no network requests** and loads no fonts, scripts, images or analytics from the internet.
- Only two things are stored locally: your theme preference (`salary-studio-theme`) and saved scenarios (`indiaSalaryCalc.scenarios.v1`).
- Clearing site data or your browser's local storage removes saved scenarios.

---

## Browser support

Use a current version of Chrome, Edge, Firefox or Safari. The interface uses modern CSS features such as `color-mix()`, `backdrop-filter` and container-friendly layouts. Internet Explorer is not supported.

The app works from a local file. If a browser blocks local storage or downloads for `file://` pages, use the optional local server described above.

---

## Known limitations

Salary Studio is an estimator, not payroll software or tax advice.

- State professional-tax figures vary and are marked **Adjustable** or **Estimate** where sources conflict. Every state and UT can be selected. Built-in slab tables cover the major levying states; where a state has no built-in table, enter the monthly PT from your payslip in the override field. Confirm with your payroll team.
- The Code on Wages 50% wage-floor rule (effective 21 November 2025) is not applied automatically. Where Basic + DA falls below half of total remuneration, PF and gratuity shown here may be a floor rather than the final employer figure.
- Employer PF administrative and EDLI charges are excluded because sources conflicted on the exact rate.
- The freelance module does not calculate GST registration or advance-tax instalments.
- The payslip is a draft generated from your inputs, not actual payroll history. No year-to-date figures are invented.
- Tax law and employer policies change. Check the rule sources in the app and confirm material decisions with a chartered accountant or your payroll department.

---

## Repository contents

| File | Purpose |
| --- | --- |
| `index.html` | The complete application: HTML, CSS, JavaScript, tax engine, UI and tests. |
| `README.md` | This guide. |
| `.nojekyll` | Lets GitHub Pages publish the repo as plain static files. |
| `.gitignore` | Ignores local tooling and OS noise. |

---

**Salary Studio** — know what actually lands in your bank account.

Built by [www.digitracks.net](https://www.digitracks.net).
