# Election Analysis in Power BI

This project is a comprehensive **Election Data Analysis** using Microsoft Excel and Power BI. It includes raw datasets, data preprocessing steps, and visual reports showcasing the performance of political parties during elections.

---

## 📁 Repository Structure

```
Election_Analysis_in_Power_BI/
│
├── 📂 Dataset
│   └── Election_Data.xlsx        # Contains raw and preprocessed election data
│
├── 📂 PowerBI Reports
│   └── Election_Analysis.pbix    # Power BI dashboard file
│
├── 📂 Screenshots
│   ├── Overview_Dashboard.png
│   ├── Statewise_Analysis.png
│   └── Party_Performance.png
│
└── README.txt                    # Project overview and instructions (this file)
```

---

## 📊 Key Features

- Import and clean raw election data in Excel.
- Create calculated fields and summaries.
- Build interactive Power BI dashboards:
  - **Overall election summary**
  - **Party-wise performance**
  - **State-wise vote distribution**
  - **Voter turnout analysis**

---

## 🛠 Tools & Technologies

- Microsoft Excel
- Microsoft Power BI
- Data Modeling (Power Query, DAX)
- Data Visualization

---

## 📌 Power BI Dashboard Highlights

- Use of slicers for filtering by year, state, and party
- Drill-through functionality for deep-dives
- Pie charts, bar graphs, and maps for better insight
- Conditional formatting for performance metrics

---

## 🚀 Getting Started

1. Clone this repository:

```bash
git clone https://github.com/arghya1501/Election_Analysis_in_Power_BI.git
```

2. Open the Excel file in `Dataset/` to view raw data.
3. Launch Power BI Desktop and open `PowerBI Reports/Election_Analysis.pbix`.
4. Refresh data to ensure the latest insights.

---

## 📝 Example Query Snippets (DAX)

```DAX
Total Votes = SUM(Election_Data[Votes])
```

```DAX
Voter Turnout % = 
DIVIDE(SUM(Election_Data[Votes]), SUM(Election_Data[Registered_Voters]), 0)
```

```DAX
Top Parties = 
TOPN(5, 
     SUMMARIZE(Election_Data, Election_Data[Party], "TotalVotes", SUM(Election_Data[Votes])), 
     [TotalVotes], 
     DESC)
```

---

## 📷 Screenshots

### 🧭 Dashboard Overview

![Overview](Screenshots/Overview_Dashboard.png)

### 📌 State-wise Analysis

![State Analysis](Screenshots/Statewise_Analysis.png)

### 🏆 Party Performance

![Party Performance](Screenshots/Party_Performance.png)

---

## 🤝 Contribution

Feel free to fork the repo and submit pull requests. Suggestions and feedback are always welcome!

---

## 📄 License

This project is licensed under the MIT License.
