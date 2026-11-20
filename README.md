# AI for Security Bootcamp - Data

Raw data files for the bootcamp notebooks, one folder per week.
Notebooks read them directly from their raw GitHub links, so nobody needs to download or upload files.

All records are **synthetic** police administrative requests for training. They do not describe real people, places, officers or incidents.

## Raw link pattern

```
https://raw.githubusercontent.com/hanyelshafey/ai-security-bootcamp-data/main/week_XX/<file>
```

## Week 07 - EDA, visualization and dashboards

| File | Rows | Used in |
| --- | --- | --- |
| `police_requests_demo.csv` | 480 | worked examples, all days |
| `police_requests_practice.csv` | 480 | exercises, Days 1-4 |
| `police_requests_project.csv` | 480 | Day 5 individual project |
| `police_requests_team.csv` | 600 | Day 5 team dashboard |
| `desk_pair_demo.csv` | 400 | Day 4 examples (Simpson's paradox) |
| `desk_pair_practice.csv` | 400 | Day 4 exercises |
| `draft_claims.json` | 4 claims | Day 4 claim verification |

Example (Python):

```python
import pandas as pd
DATA_URL = "https://raw.githubusercontent.com/hanyelshafey/ai-security-bootcamp-data/main/week_07/"
requests = pd.read_csv(DATA_URL + "police_requests_practice.csv", parse_dates=["opened_at"])
```

## Week 08 - Introduction to machine learning and police data analysis project

| File | Rows | Used in |
| --- | --- | --- |
| `requests_demo.csv` | 360 | Days 1-2 worked examples |
| `requests_practice.csv` | 480 | Days 1-2 exercises |
| `ml_scenarios.json` | 16 cards | Day 1 problem framing (no answers inside) |
| `leakage_clinic.csv` | 344 | Day 2 leakage clinic (planted duplicates, a label-revealing column, a future-looking feature) |
| `reports_demo.csv` | 432 | Day 3 worked examples (raw, planted defects) |
| `reports_practice.csv` | 618 | Day 3 exercises (raw, planted defects) |
| `service_records_demo.csv` | 1159 | Day 3 worked examples (raw, planted defects) |
| `service_records_practice.csv` | 1667 | Day 3 exercises (raw, planted defects) |
| `desks.csv` | 6 | Day 3 desk lookup |
| `sla_targets.csv` | 3 | Day 3 target hours to first action (training values, not official standards) |

Example (Python):

```python
import pandas as pd
DATA_URL = "https://raw.githubusercontent.com/hanyelshafey/ai-security-bootcamp-data/main/week_08/"
requests = pd.read_csv(DATA_URL + "requests_practice.csv", parse_dates=["opened_at", "first_action_at", "completed_at"])
```
