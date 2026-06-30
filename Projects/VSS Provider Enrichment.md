# VSS Provider Enrichment Project

> Enriching 7,799 healthcare provider records for Emperious outreach pipeline.

---

## Objective
Enrich all rows in the **"Complete List"** tab of VSS_Emperious.xlsx with verified contact data. All new/corrected values written in **blue font (ARGB: FF0000FF)** for traceability.

## Status
- **Total rows:** ~7,799 providers
- **Completed:** ~875 rows (~11%) — last confirmed row: 875
- **Next batch:** Row 876 onward
- **Resume command:** *"Continue from row 876"*

## Fields Being Enriched
| Col | Field |
|---|---|
| A | Provider Name |
| B | Specialty |
| C | Phone |
| D | Email |
| E | Address |
| F | City |
| G | State |
| H | Website |
| I | LinkedIn |
| J | Other Social (Doximity) |

## Priority Fields
Phone · Email · LinkedIn (col I) · Doximity (col J) · Website (col H)

## Research Sources
1. **Doximity** — best for MD/DO/PA profiles
2. **Healthgrades** — verification
3. **Practice websites**
4. **LinkedIn**

## Files
- Source: VSS_Emperious.xlsx (Google Sheets)
- Output: [VSS_Emperious_enriched_v2 (Google Drive)](https://docs.google.com/spreadsheets/d/1YUe-BVVQUXrVhanNJakwve9tTgx0VdWEr3-dIN_Kk5s/edit)

## Data Quality Rules
- Bad data → replace with **Not Found** in blue
- Duplicates → flag as *DUPLICATE - see Row X* in col J
- Skip: blank col A, email addresses in name field, placeholders

## Related
- [[Emperious Healthcare]]
- [[MOC — Business]]
