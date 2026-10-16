# India-Stocks-991-1020-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 991 to 1020)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-991-1020-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (991 to 1020)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 991 | `DONEAR` | Donear Industries Limited | `DONEAR.NS` |
| 992 | `DPABHUSHAN` | D. P. Abhushan Limited | `DPABHUSHAN.NS` |
| 993 | `DPSCLTD` | DPSC Limited | `DPSCLTD.NS` |
| 994 | `DPWIRES` | D P Wires Limited | `DPWIRES.NS` |
| 995 | `DRAGARWQ` | Dr Agarwals Eye Hospital Limited | `DRAGARWQ.NS` |
| 996 | `DRCSYSTEMS` | DRC Systems India Limited | `DRCSYSTEMS.NS` |
| 997 | `DREAMFOLKS` | Dreamfolks Services Limited | `DREAMFOLKS.NS` |
| 998 | `DREDGECORP` | Dredging Corporation of India Limited | `DREDGECORP.NS` |
| 999 | `DSFCL` | DCM Shriram Fine Chemicals Limited | `DSFCL.NS` |
| 1000 | `DSKULKARNI` | DS Kulkarni Developers Limited | `DSKULKARNI.NS` |
| 1001 | `DSSL` | Dynacons Systems & Solutions Limited | `DSSL.NS` |
| 1002 | `DTIL` | Dhunseri Tea & Industries Limited | `DTIL.NS` |
| 1003 | `DUCON` | Ducon Infratechnologies Limited | `DUCON.NS` |
| 1004 | `DVL` | Dhunseri Ventures Limited | `DVL.NS` |
| 1005 | `DWARKESH` | Dwarikesh Sugar Industries Limited | `DWARKESH.NS` |
| 1006 | `DYCL` | Dynamic Cables Limited | `DYCL.NS` |
| 1007 | `DYNAMATECH` | Dynamatic Technologies Limited | `DYNAMATECH.NS` |
| 1008 | `DYNPRO` | Dynemic Products Limited | `DYNPRO.NS` |
| 1009 | `E2E` | E2E Networks Limited | `E2E.NS` |
| 1010 | `EASEMYTRIP` | Easy Trip Planners Limited | `EASEMYTRIP.NS` |
| 1011 | `EASTSILK` | Eastern Silk Industries Limited | `EASTSILK.NS` |
| 1012 | `EASTWEST` | East West Freight Carriers Limited | `EASTWEST.NS` |
| 1013 | `EBGNG` | GNG Electronics Limited | `EBGNG.NS` |
| 1014 | `EBIX` | EBIX Limited | `EBIX.NS` |
| 1015 | `ECORECO` | Eco Recycling Limited | `ECORECO.NS` |
| 1016 | `ECOSMOBLTY` | Ecos (India) Mobility & Hospitality Limited | `ECOSMOBLTY.NS` |
| 1017 | `EDELWEISS` | Edelweiss Financial Services Limited | `EDELWEISS.NS` |
| 1018 | `EFCIL` | EFC (I) Limited | `EFCIL.NS` |
| 1019 | `EIEL` | Enviro Infra Engineers Limited | `EIEL.NS` |
| 1020 | `EIFFL` | Euro India Fresh Foods Limited | `EIFFL.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream DONEAR 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-991-1020-Historical-Data/main/DONEAR/1m/2026/10/DONEAR_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
