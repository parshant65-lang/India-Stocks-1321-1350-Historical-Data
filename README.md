# India-Stocks-1321-1350-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 1321 to 1350)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-1321-1350-Historical-Data/
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

## 📦 Constituents (1321 to 1350)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 1321 | `INDOBORAX` | Indo Borax & Chemicals Limited | `INDOBORAX.NS` |
| 1322 | `INDOCO` | Indoco Remedies Limited | `INDOCO.NS` |
| 1323 | `INDOFARM` | Indo Farm Equipment Limited | `INDOFARM.NS` |
| 1324 | `INDOKEM` | Indokem Limited | `INDOKEM.NS` |
| 1325 | `INDOMIM` | INDO-MIM Limited | `INDOMIM.NS` |
| 1326 | `INDORAMA` | Indo Rama Synthetics (India) Limited | `INDORAMA.NS` |
| 1327 | `INDOSTAR` | IndoStar Capital Finance Limited | `INDOSTAR.NS` |
| 1328 | `INDOTECH` | Indo Tech Transformers Limited | `INDOTECH.NS` |
| 1329 | `INDOTHAI` | Indo Thai Securities Limited | `INDOTHAI.NS` |
| 1330 | `INDOUS` | Indo Us Biotech Limited | `INDOUS.NS` |
| 1331 | `INDOWIND` | Indowind Energy Limited | `INDOWIND.NS` |
| 1332 | `INDPRUD` | Industrial & Prudential Investment Company Limited | `INDPRUD.NS` |
| 1333 | `INDRAMEDCO` | Indraprastha Medical Corporation Limited | `INDRAMEDCO.NS` |
| 1334 | `INDSWFTLAB` | Ind-Swift Laboratories Limited | `INDSWFTLAB.NS` |
| 1335 | `INDTERRAIN` | Indian Terrain Fashions Limited | `INDTERRAIN.NS` |
| 1336 | `INFOBEAN` | InfoBeans Technologies Limited | `INFOBEAN.NS` |
| 1337 | `INFOMEDIA` | Infomedia Press Limited | `INFOMEDIA.NS` |
| 1338 | `INGERRAND` | Ingersoll Rand (India) Limited | `INGERRAND.NS` |
| 1339 | `INNOVACAP` | Innova Captab Limited | `INNOVACAP.NS` |
| 1340 | `INNOVANA` | Innovana Thinklabs Limited | `INNOVANA.NS` |
| 1341 | `INNOVISION` | Innovision Limited | `INNOVISION.NS` |
| 1342 | `INOXGREEN` | Inox Green Energy Services Limited | `INOXGREEN.NS` |
| 1343 | `INSECTICID` | Insecticides (India) Limited | `INSECTICID.NS` |
| 1344 | `INSPIRISYS` | Inspirisys Solutions Limited | `INSPIRISYS.NS` |
| 1345 | `INTENTECH` | Intense Technologies Limited | `INTENTECH.NS` |
| 1346 | `INTERARCH` | Interarch Building Solutions Limited | `INTERARCH.NS` |
| 1347 | `INTLCONV` | International Conveyors Limited | `INTLCONV.NS` |
| 1348 | `INVENTURE` | Inventure Growth & Securities Limited | `INVENTURE.NS` |
| 1349 | `INVPRECQ` | Investment & Precision Castings Limited | `INVPRECQ.NS` |
| 1350 | `IOLCP` | IOL Chemicals and Pharmaceuticals Limited | `IOLCP.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream INDOBORAX 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-1321-1350-Historical-Data/main/INDOBORAX/1m/2026/10/INDOBORAX_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
