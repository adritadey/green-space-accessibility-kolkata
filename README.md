# 🌳 Green Space Accessibility for Seniors – Kolkata

## 📌 Overview
This Power BI dashboard analyzes how accessible public parks are for senior citizens across Kolkata. It compares walkability, seating, shade, and proximity to hospitals to highlight equity gaps in urban green space design.

## 🎯 Objective
- Evaluate senior-friendly features across major parks
- Visualize disparities using Power BI
- Rank parks using a custom Accessibility Index

## 🛠️ Tools Used
- Power BI Desktop
- DAX for calculated metrics
- Excel for data preparation

## 🗂️ Dataset Description
| Park Name           | Neighborhood     | Distance to Hospital (km) | Seating | Shade   | Walkability Score | Senior Visits/Day |
|---------------------|------------------|----------------------------|---------|---------|--------------------|--------------------|
| Rabindra Sarobar    | Lake Gardens     | 0.4                        | Yes     | Yes     | 9                  | 120                |
| Deshapriya Park     | Ballygunge       | 1.2                        | Yes     | No      | 7                  | 80                 |
| Eco Park            | New Town         | 2.5                        | Yes     | Yes     | 6                  | 60                 |
| Mohor Kunja         | Maidan           | 0.6                        | No      | Yes     | 8                  | 45                 |
| Kumartuli Garden    | Kumartuli        | 1.8                        | No      | No      | 5                  | 20                 |
| Park Circus Maidan  | Park Circus      | 1.0                        | Yes     | Partial | 7                  | 70                 |

## 📊 Dashboard Features
- Bar chart: Senior visits per park
- Scatter plot: Walkability vs senior usage
- Stacked column chart: Seating and shade availability
- Slicers: Filter by amenities and hospital proximity
- Accessibility Index calculated using DAX

## 🧮 DAX Formula
```DAX
AccessibilityIndex = 
([Walkability Score] + 
IF([Seating] = "Yes", 1, 0) + 
IF([Shade] = "Yes", 1, 0)) 
/ [Distance to Hospital (km)]
📁 Repository Structure
/
├── GreenSpaceAccessibility.pbix        # Power BI dashboard file
├── README.md                           # Project overview
├── .gitignore                          # Git tracking exclusions
└── /screenshots                        # Dashboard visuals
    ├── dashboard-overview.png
    ├── scatter-plot.png
    └── stacked-chart.png
🧠 Key Insights
Rabindra Sarobar ranks highest in accessibility and senior engagement

Kumartuli Garden lacks basic amenities and has the lowest usage

Park Circus Maidan shows potential for community-driven improvements

🌿 Recommendations
Improve seating and shade in underserved parks

Prioritize walkability and healthcare proximity in future park designs

Use accessibility index to guide inclusive urban planning
