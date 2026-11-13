# Smart Financial Management — V1.8

Bilingual (Spanish/English) financial-costing prototype for digital marketing agencies.

## V1.8 — Invoicing, customer-specific withholdings and collections
- Replaces campaign analytics navigation with a financial invoicing and collections module.
- Configure multiple withholding items per customer; customers can have different configurations.
- Supports per-thousand rates (e.g. 9.66‰) and percentage rates (e.g. 11%, 4%, 3.5%).
- Each withholding can use the invoice tax base or its own explicitly entered taxable base.
- Invoice form loads that customer's configured withholdings; the user can toggle them per invoice.
- Calculates VAT, total withholdings, expected net cash and actual collection separately.
- Keeps profit/cash distinction: VAT is shown separately and is not treated as agency service revenue.
- Demo invoice and withholding records are stored only in this browser using localStorage.

## Calculation rules
- 9.66 per thousand: taxable base × 9.66 / 1,000.
- Percentage withholding: taxable base × rate / 100.
- Expected net cash: invoice taxable base + VAT − applicable withholdings.
- Withholding selection is customer-specific and may be adjusted on each invoice. The prototype does not decide legal applicability or tax bases; users must configure them according to the applicable certificate and tax treatment.

## Important limitations
This remains a front-end demonstration, not accounting or tax software. It does not validate Colombian tax obligations, determine whether a withholding applies, calculate tax bases from legal rules, connect to DIAN/SIIGO/banks, or synchronize across users. The VAT rate is editable per invoice. Use synthetic data only. All data is local to the current browser.

## Publish on GitHub Pages
Replace `docs/index.html` and `docs/README.md` with these files. Preserve `docs/PROJECT_ROADMAP.md` and keep Pages configured to `/docs`. Commit, then refresh the site with Ctrl+Shift+R.
