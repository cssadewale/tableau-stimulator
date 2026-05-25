# Sample Data Guide — Tableau Stimulator Enterprise

Five ready-to-use CSV datasets plus enterprise chart suggestions.

## How to Use

1. Copy any CSV block below
2. Paste into a text editor, save as `.csv`
3. Upload to Tableau Stimulator Enterprise
4. Or click **Sample Data** in the menu strip for the built-in dataset

---

## Sample 1 — Regional Sales Performance (24 rows)

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

**Enterprise chart suggestions:**
- 🌳 **Treemap:** Region (COLS) → Sales (ROWS) — proportional area by region
- 🌹 **Rose:** Month (COLS) → Sales (ROWS) — cyclical sales pattern
- ▰ **Bullet:** Region (COLS) → Sales (ROWS), Goal=500000 — actual vs target
- 📊 **Histogram:** Sales (ROWS) — distribution of all sales values

---

## Sample 2 — Student Performance (30 rows)

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

**Enterprise chart suggestions:**
- 📈 **Regression:** Attendance_Pct (X) → Score (Y) — does attendance predict performance?
- 🎯 **Clustering:** Score vs Study_Hours — group students by engagement
- ⚪ **Bubble:** Attendance_Pct (X) → Score (Y), Size=Study_Hours
- ═ **Parallel Coords** — multi-variable student profile comparison

---

## Creator / Owner
**Adewale Samson Adeagbo** — Data Scientist, STEM Educator, Lagos, Nigeria
- Portfolio: https://cssadewale.pages.dev | HMG Concepts: https://hmgconcepts.pages.dev | HMG Academy: https://hmgacademy.pages.dev
- GitHub: https://github.com/cssadewale | Email: hmgconcepts@gmail.com | WhatsApp: +234 810 086 6322
