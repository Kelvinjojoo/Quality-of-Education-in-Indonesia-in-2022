# 📊 Quality of Education in Indonesia (2022)

This Shiny dashboard explores educational conditions in Indonesia using data from 2022. It focuses on the **distribution of teachers**, **school participation**, **poverty vs education correlation**, and **library infrastructure**, aligning with **Sustainable Development Goal 4 (SDG 4)**:  
> _"Ensure inclusive and equitable quality education and promote lifelong learning opportunities for all."_

---

## 👥 Team Members

- Aaron Winston Gho – 2702210522  
- Aldo Oktavianus – 2702234081  
- Kelvin Jonathan Yusach – 2702209533  
- Nicholas Ananda Heryanto – 2702213695  
- Tyrone Yutanesy Iman – 2702211512  

---

## 📁 Project Overview

The dashboard provides the following visual insights:

| Feature | Description |
|--------|-------------|
| **📚 Teacher Distribution** | Bar chart of teacher counts by education level (SD, SMP, SMA, SMK) by province |
| **📈 School Participation Trends** | Line chart of participation by age group (7–24 years) from 2002–2022 |
| **📉 Education vs Poverty** | Scatter plot showing relationship between educational attainment and poverty rate |
| **🏫 Library Access** | Top/bottom 5 provinces with highest/lowest number of libraries |

---

## 🧼 Data Cleaning Highlights

All preprocessing is done in R using the following techniques:

- **Missing Data**  
  - Character variables: replaced with `"Unknown"`  
  - Numeric variables: filled with **median** value to preserve data distribution

- **Duplicate Records**  
  - Removed using `distinct()`

- **Outlier Detection**  
  - Handled via **IQR** and **Z-score** custom functions

- **Column Standardization**  
  - Province names normalized (e.g., `"Prov. DKI Jakarta"` → `"dki jakarta"`, `"Kep." → "Kepulauan"`)

- **Dataset Merging**  
  - Education and poverty datasets merged using `Provinsi` as a key

---

## 💻 How to Run

### Requirements

Install the required R packages:

```r
install.packages(c("shiny", "plotly", "ggplot2", "dplyr", "readxl", "bslib"))
