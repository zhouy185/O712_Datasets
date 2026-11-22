# Admission offers data (simulated)

Simulated data for the BUSADMIN O712 lesson on scholarships, offer acceptance, and offer optimization. No real applicants.

| File | Rows | Description |
|---|---|---|
| `admissions_history.csv` | 3,000 | Past offers, 2022–2026. `enrolled` = 1 if the applicant accepted the offer. |
| `admissions_2027.csv` | 197 | Eligible applicants this year (no outcome). |
| `admissions_2027_predictions.csv` | 197 | Output of Part 1: merit index, planned scholarship, and predicted acceptance probability (`p_accept` at the planned scholarship; `p_tier_0`, `p_tier_5000`, `p_tier_10000` at each scholarship tier). Input to Part 2. |
| `admissions_2027_p_accept.csv` | 197 | `applicant_id`, `merit_index`, `p_accept` (acceptance probability at the planned scholarship). Input for choosing offers. |
| `admissions_2027_p_tiers.csv` | 197 | `applicant_id`, `merit_index`, `p_tier_0`, `p_tier_5000`, `p_tier_10000` (acceptance probability at each scholarship tier). Input for choosing offers and scholarships. |

**Columns:** `applicant_id`, `admission_cohort`, `gpa`, `gmat_score`, `work_experience_years`, `distance_km`, `international` (0/1), `campus_visit` (0/1), `early_applicant` (0/1), `scholarship_offer_usd`, `enrolled` (history only).

Load in Python:

```python
import pandas as pd
DATA = "https://raw.githubusercontent.com/zhouy185/O712_Datasets/main/admission/"
hist = pd.read_csv(DATA + "admissions_history.csv")
app  = pd.read_csv(DATA + "admissions_2027.csv")
```
