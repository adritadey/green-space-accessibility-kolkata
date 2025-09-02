# 🌳 Green Space Accessibility for Seniors – Kolkata

## 📌 Overview
This project analyzes how accessible public parks are for senior citizens across various neighborhoods in Kolkata, India. Using real-world spatial and amenity data, the dashboard compares parks based on walkability, seating, shade, and proximity to healthcare facilities.

## 🎯 Objective
- Evaluate senior-friendly features across major parks in Kolkata
- Use Power BI to visualize disparities in accessibility
- Create a custom accessibility index to rank parks and identify underserved areas

## 🛠️ Tools Used
- **Power BI Desktop** – Dashboard creation and data modeling
- **DAX** – Custom accessibility index calculation
- **Excel/CSV** – Data preparation and import

## 🗂️ Dataset Description
| Park Name           | Neighborhood     | Distance to Hospital (km) | Seating | Shade | Walkability Score (0–10) | Senior Visits/Day |
|---------------------|------------------|----------------------------|---------|-------|---------------------------|--------------------|
| Rabindra Sarobar    | Lake Gardens     | 0.4                        | Yes     | Yes   | 9                         | 120                |
| Deshapriya Park     | Ballygunge       | 1.2                        | Yes     | No    | 7                         | 80                 |
| Eco Park            | New Town         | 2.5                        | Yes     | Yes   | 6                         | 60                 |
| Mohor Kunja         | Maidan           | 0.6                        | No      | Yes   | 8                         | 45                 |
| Kumartuli Garden    | Kumartuli        | 1.8                        | No      | No    | 5                         | 20                 |
| Park Circus Maidan  | Park Circus      | 1.0                        | Yes     | Partial | 7                       | 70                 |

## 📊 Dashboard Features
- **Bar Chart**: Senior visits per park
- **Map Visual**: Park locations with accessibility scores
- **Stacked Column Chart**: Seating and shade availability
- **Scatter Plot**: Walkability vs senior usage
- **Slicers**: Filter parks by amenities and hospital proximity

## 🧮 Accessibility Index (DAX Formula)
```DAX
AccessibilityIndex = 
([Walkability Score] + 
IF([Seating] = "Yes", 1, 0) + 
IF([Shade] = "Yes", 1, 0)) 
/ [Distance to Hospital (km)]

🧠 Key Insights
Rabindra Sarobar ranks highest in accessibility and senior engagement

Kumartuli Garden lacks basic amenities and has the lowest usage

Park Circus Maidan shows potential for community-driven improvements

🌿 Recommendations
Improve seating and shade in underserved parks

Prioritize walkability and healthcare proximity in future park designs

Use accessibility index to guide inclusive urban planning
