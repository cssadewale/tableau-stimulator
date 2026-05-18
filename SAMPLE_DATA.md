# Sample Data Guide

Five ready-to-use CSV datasets you can copy and use to test DataViz Studio
immediately after deployment, without needing your own data.

---

## How to Use

1. Copy any CSV block below
2. Paste it into a plain text editor (Notepad, Gedit, or any editor)
3. Save with a `.csv` extension (e.g. `sales_data.csv`)
4. Upload to DataViz Studio via the upload zone in the left pane

---

## Sample 1 — Regional Sales Performance

**Rows:** 24 | **Numeric fields:** Sales, Target, Profit, Units_Sold

```csv
Region,Month,Sales,Target,Profit,Units_Sold,Sales_Rep
Lagos,Jan,450000,400000,112500,180,Chidi Okonkwo
Abuja,Jan,380000,350000,95000,152,Amina Bello
Port Harcourt,Jan,310000,300000,77500,124,Emeka Nwosu
Kano,Jan,280000,280000,70000,112,Fatima Sule
Lagos,Feb,520000,420000,130000,208,Chidi Okonkwo
Abuja,Feb,410000,370000,102500,164,Amina Bello
Port Harcourt,Feb,350000,320000,87500,140,Emeka Nwosu
Kano,Feb,290000,290000,72500,116,Fatima Sule
Lagos,Mar,480000,450000,120000,192,Chidi Okonkwo
Abuja,Mar,440000,400000,110000,176,Amina Bello
Port Harcourt,Mar,320000,330000,80000,128,Emeka Nwosu
Kano,Mar,305000,295000,76250,122,Fatima Sule
Lagos,Apr,560000,480000,140000,224,Chidi Okonkwo
Abuja,Apr,390000,380000,97500,156,Amina Bello
Port Harcourt,Apr,410000,350000,102500,164,Emeka Nwosu
Kano,Apr,320000,310000,80000,128,Fatima Sule
Lagos,May,610000,500000,152500,244,Chidi Okonkwo
Abuja,May,450000,410000,112500,180,Amina Bello
Port Harcourt,May,380000,360000,95000,152,Emeka Nwosu
Kano,May,340000,320000,85000,136,Fatima Sule
Lagos,Jun,590000,520000,147500,236,Chidi Okonkwo
Abuja,Jun,470000,430000,117500,188,Amina Bello
Port Harcourt,Jun,395000,370000,98750,158,Emeka Nwosu
Kano,Jun,355000,330000,88750,142,Fatima Sule
```

**Suggested Charts:**
- Bar chart: Region (COLS) → Sales (ROWS), Agg=SUM — regional totals
- Line chart: Month (COLS) → Sales + Target (ROWS), Dual Axis ON — trend vs target
- Waterfall: Month (COLS) → Profit (ROWS) — monthly profit waterfall
- Pivot: Row=Region, Col=Month, Value=Sales — full matrix
- Goal Line: Set 500000 as monthly revenue target

---

## Sample 2 — Student Performance Tracker

**Rows:** 30 | **Numeric fields:** Score, Study_Hours, Attendance_Pct

```csv
Student_ID,Name,Subject,Score,Grade,Class,Gender,Attendance_Pct,Study_Hours
S001,Adaeze Obi,Mathematics,82,B,JSS3,Female,94,4.5
S001,Adaeze Obi,English,76,C,JSS3,Female,94,3.0
S001,Adaeze Obi,Science,88,A,JSS3,Female,94,5.0
S002,Tunde Adesanya,Mathematics,91,A,JSS3,Male,88,6.0
S002,Tunde Adesanya,English,84,B,JSS3,Male,88,4.0
S002,Tunde Adesanya,Science,79,C,JSS3,Male,88,3.5
S003,Halima Yusuf,Mathematics,65,D,JSS3,Female,72,2.0
S003,Halima Yusuf,English,71,C,JSS3,Female,72,2.5
S003,Halima Yusuf,Science,68,D,JSS3,Female,72,2.0
S004,Chukwuemeka Eze,Mathematics,95,A,SSS1,Male,98,7.0
S004,Chukwuemeka Eze,English,89,A,SSS1,Male,98,5.5
S004,Chukwuemeka Eze,Science,92,A,SSS1,Male,98,6.5
S005,Blessing Nwosu,Mathematics,73,C,SSS1,Female,85,3.5
S005,Blessing Nwosu,English,80,B,SSS1,Female,85,4.0
S005,Blessing Nwosu,Science,77,C,SSS1,Female,85,3.0
S006,Ibrahim Mohammed,Mathematics,58,E,JSS2,Male,65,1.5
S006,Ibrahim Mohammed,English,62,D,JSS2,Male,65,2.0
S006,Ibrahim Mohammed,Science,55,E,JSS2,Male,65,1.5
S007,Ngozi Okafor,Mathematics,87,B,SSS2,Female,91,5.0
S007,Ngozi Okafor,English,93,A,SSS2,Female,91,6.0
S007,Ngozi Okafor,Science,85,B,SSS2,Female,91,4.5
S008,Babatunde Lawal,Mathematics,70,C,SSS2,Male,79,3.0
S008,Babatunde Lawal,English,74,C,SSS2,Male,79,3.5
S008,Babatunde Lawal,Science,72,C,SSS2,Male,79,2.5
S009,Kemi Adeyemi,Mathematics,96,A,SSS3,Female,99,8.0
S009,Kemi Adeyemi,English,94,A,SSS3,Female,99,7.5
S009,Kemi Adeyemi,Science,97,A,SSS3,Female,99,8.0
S010,Olatunde Gbadebo,Mathematics,61,D,SSS3,Male,70,2.0
S010,Olatunde Gbadebo,English,67,D,SSS3,Male,70,2.5
S010,Olatunde Gbadebo,Science,64,D,SSS3,Male,70,1.5
```

**Suggested Charts:**
- Box Plot: Subject (COLS) → Score (ROWS) — distribution per subject
- Scatter: Attendance_Pct (COLS) → Score (ROWS) — correlation: attendance vs performance
- Bar: Class (COLS) → Score (ROWS), Color By=Subject, Agg=AVG
- Pivot: Row=Class, Col=Subject, Value=Score, Agg=AVG
- Statistics Tab: Run Statistics on Score, Attendance_Pct, Study_Hours

---

## Sample 3 — HR Employee Data (with missing value for Data Cleaner testing)

**Rows:** 25 | **Note:** Row E025 has a missing Burn_Rate — test the Data Cleaner with this

```csv
Employee_ID,Department,Gender,Age,Years_Experience,Salary,Burn_Rate,Satisfaction_Score,Attrition
E001,Engineering,Male,28,4,580000,0.42,3.8,No
E002,Engineering,Female,34,8,720000,0.61,3.2,No
E003,Sales,Male,26,2,420000,0.55,3.5,Yes
E004,Sales,Female,31,6,490000,0.48,4.1,No
E005,HR,Female,29,5,380000,0.35,4.5,No
E006,HR,Male,38,12,450000,0.39,4.2,No
E007,Finance,Male,42,16,850000,0.52,3.6,No
E008,Finance,Female,35,9,760000,0.58,3.0,Yes
E009,Engineering,Male,25,1,520000,0.71,2.9,Yes
E010,Engineering,Female,30,6,640000,0.44,4.0,No
E011,Sales,Male,27,3,440000,0.63,3.1,Yes
E012,Sales,Female,33,7,510000,0.41,4.3,No
E013,Marketing,Female,28,4,460000,0.38,4.6,No
E014,Marketing,Male,36,10,620000,0.50,3.7,No
E015,Finance,Male,44,18,920000,0.46,3.9,No
E016,Engineering,Female,32,7,700000,0.67,2.7,Yes
E017,HR,Female,26,2,350000,0.32,4.8,No
E018,Sales,Male,29,4,455000,0.59,3.3,Yes
E019,Marketing,Male,40,14,680000,0.43,4.0,No
E020,Finance,Female,37,11,810000,0.55,3.4,No
E021,Engineering,Male,23,1,490000,0.74,2.5,Yes
E022,Sales,Female,35,8,530000,0.45,4.2,No
E023,HR,Male,31,6,410000,0.36,4.4,No
E024,Marketing,Female,27,3,480000,0.40,4.7,No
E025,Engineering,Male,45,20,980000,,3.8,No
```

**Suggested Charts:**
- Bar: Department (COLS) → Salary (ROWS), Agg=AVG — average salary per department
- Box Plot: Department (COLS) → Burn_Rate (ROWS) — burnout distribution
- Funnel: Department (COLS) → Attrition count — attrition by department
- Data Cleaner Tab: Scan → will detect 1 missing value in Burn_Rate → click Fix to fill with mean
- Statistics Tab: Run Statistics on Salary, Age, Burn_Rate, Satisfaction_Score

---

## Sample 4 — Sales Funnel / Conversion Pipeline

**Rows:** 8 | **Use for:** Funnel Chart, Gauge, KPI Cards

```csv
Stage,Leads,Conversion_Rate,Revenue,Target_Revenue
Awareness,12500,100.0,0,0
Interest,8200,65.6,0,0
Consideration,4100,50.0,0,0
Intent,1850,45.1,0,0
Evaluation,920,49.7,0,0
Purchase,380,41.3,7600000,8000000
Retention,290,76.3,5800000,6000000
Advocacy,180,62.1,3600000,4000000
```

**Suggested Charts:**
- Funnel: Stage (COLS) → Leads (ROWS) — full conversion funnel
- Gauge: Revenue (ROWS), Agg=SUM — total revenue as a speedometer
- Bar: Stage (COLS) → Conversion_Rate (ROWS) — conversion rate per stage
- Goal Line: Set 8000000 as the purchase stage revenue target

---

## Sample 5 — Monthly Financial Summary

**Rows:** 12 | **Use for:** Waterfall, Line with Dual Axis, Trend Line

```csv
Month,Revenue,COGS,Gross_Profit,Operating_Expenses,Net_Profit,Headcount
Jan,2100000,1050000,1050000,630000,420000,45
Feb,1950000,975000,975000,620000,355000,45
Mar,2300000,1150000,1150000,640000,510000,47
Apr,2450000,1225000,1225000,660000,565000,47
May,2600000,1300000,1300000,680000,620000,50
Jun,2800000,1400000,1400000,700000,700000,52
Jul,2550000,1275000,1275000,710000,565000,52
Aug,2400000,1200000,1200000,720000,480000,52
Sep,2750000,1375000,1375000,730000,645000,54
Oct,3100000,1550000,1550000,750000,800000,55
Nov,3400000,1700000,1700000,770000,930000,57
Dec,3800000,1900000,1900000,800000,1100000,60
```

**Suggested Charts:**
- Waterfall: Month (COLS) → Net_Profit (ROWS) — profit changes across the year
- Line: Month (COLS) → Revenue + Net_Profit (ROWS), Dual Axis ON
- Line + Trend: Month (COLS) → Revenue (ROWS), click the Trend button
- Goal Line: Set 3000000 as the monthly revenue target

---

## Public Datasets for Further Testing

| Dataset | Source | Rows | Good For |
|---|---|---|---|
| Iris Dataset | UCI ML Repository | 150 | Scatter, Box Plot, Statistics |
| Titanic Passenger Data | Kaggle | 891 | Bar, Pivot, Cleaner |
| Nigeria States Population | OpenAfrica | 37 | Bar, Heatmap, Map |
| World Population | Kaggle | 234 | Bar, Rankings, Trend |
| COVID-19 Time Series | Our World in Data | Varies | Line, Area, Trend |

---

## Tips for Your Own CSV Files

1. **First row must be column headers** — no merged cells, no blank headers
2. **Consistent data types per column** — do not mix numbers and text in the same column
3. **UTF-8 encoding** when saving from Excel: File → Save As → CSV UTF-8 (Comma delimited)
4. **No merged cells** — DataViz Studio reads flat tabular data only
5. **Missing values** — empty cells are fine; the Data Cleaner handles them

**From Excel:** File → Save As → CSV UTF-8 (Comma delimited) → Save

**From Google Sheets:** File → Download → Comma Separated Values (.csv)

**From Python:**
```python
df.to_csv("my_data.csv", index=False, encoding="utf-8")
```
