# course-data

Public, data-only repository for the Data Analytics with Python course
(`DataAnalyticsClassFall2026`). Holds the raw dataset for each week so every
student's per-week assignment repo can fetch it at runtime instead of
carrying its own copy — "Use this template" on a week's repo duplicates
whatever's committed there, so keeping data out of those repos keeps
storage sane across a full class of students.

This repo is intentionally public (no student work lives here, just public
source data) so files can be fetched with a plain, unauthenticated URL.

## Fetching a file

Build the raw URL as:

```
https://raw.githubusercontent.com/DataAnalyticsClassFall2026/course-data/main/<path>
```

For example, in a notebook:

```python
import pandas as pd

url = "https://raw.githubusercontent.com/DataAnalyticsClassFall2026/course-data/main/week01/hurricane_season.csv"
df = pd.read_csv(url)
```

## Contents

| Folder | Week | Dataset | Notes |
|---|---|---|---|
| `week01/` | 1 | North Atlantic hurricane best-track data (1980-2026) | Trimmed from the full global IBTrACS archive to the `NA` basin and a core set of columns to stay well under GitHub's 100MB file limit. |
| `week02/` | 2 | PISA 2025 results | Two source spreadsheets. |
| `week03/` | 3 | FIFA World Cup historical records | ~26 relational tables (matches, players, goals, teams, referees, etc.). |
| `week04/` | 4 | Hantavirus surveillance data | Single spreadsheet. |
| `week05/` | 5 | US-Canada trade data | One CSV per month, Jul 2025 - Jun 2026. |
| `week06/` | 6 | FEMA disaster declarations | Single Parquet file. |
| `week07/` | 7 | Surveillance technology dataset | Single CSV. |
| `week08/` | 8 | AI incident/classification data | Two BSON files. |
| `week09/` | 9 | Occupational employment statistics | Two large spreadsheets (used for a Pandas-vs-Polars performance comparison). |

Week 10 has no dataset here by design — it's a student-chosen capstone dataset.

## Source data

Datasets were sourced from public government/organizational data (NOAA,
OECD/PISA, FIFA records, CDC/public health surveillance, US-Canada trade
statistics, FEMA, and public AI-incident reporting). No proprietary or
licensed exercise content is reproduced here — only the underlying public
data each week's assignment analyzes.
