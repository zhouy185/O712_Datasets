# Admission offers data (simulated)

Simulated data for the BUSADMIN O712 lesson on scholarships, offer acceptance, and offer optimization. No real applicants.

| File | Rows | Description |
|---|---|---|
| `admissions_history.csv` | 3,000 | Past offers, 2022–2026. `enrolled` = 1 if the applicant accepted the offer. |
| `admissions_2027.csv` | 197 | Eligible applicants this year (no outcome). |

**Columns:** `applicant_id`, `admission_cohort`, `gpa`, `gmat_score`, `work_experience_years`, `distance_km`, `international` (0/1), `campus_visit` (0/1), `early_applicant` (0/1), `scholarship_offer_usd`, `enrolled` (history only).

Load in Python:

```python
import pandas as pd
DATA = "https://raw.githubusercontent.com/zhouy185/O712_Datasets/main/admission/"
hist = pd.read_csv(DATA + "admissions_history.csv")
app  = pd.read_csv(DATA + "admissions_2027.csv")
```
