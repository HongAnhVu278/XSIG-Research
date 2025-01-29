# XSIG-Research
# 🌳 Parks and COVID-19: What's the Connection?

## **Overview**
During the COVID-19 pandemic, outdoor activities became a crucial alternative to indoor venues due to high transmission risks. Urban green spaces, such as parks, saw increased usage, raising questions about their potential role in public health. While many assume that greater park access leads to lower infection rates, **this study investigates whether there is a measurable correlation between green space availability and COVID-19 severity.**

This research **analyzes geospatial data** to examine whether counties with larger park areas experienced **lower COVID-19 cases and death rates per capita**.

---

## **Motivation**
The project is inspired by ongoing discussions on the role of **public spaces in health outcomes**. While studies often focus on long-term urban planning post-pandemic, **this research provides a preliminary analysis of how green space access influenced COVID-19 case severity during the pandemic.** 

More details on my research motivation and process can be found in my blog post:  
[🔗 Parks and COVID-19: What’s the Connection?](https://xsigsummer.wordpress.com/2023/06/16/parks-and-covid-19-whats-the-connection/)

---

## **Data and Methodology**
### **📊 Datasets Used**
1. **ParkServe (Trust for Public Land - TPL)**
   - Contains geospatial data on public park locations across the U.S.
   - Data was collected from local authorities and GIS open-source platforms.

2. **USAFacts COVID-19 Data**
   - Provides county-level **confirmed cases and deaths** across the U.S.
   - Cumulative case and death counts were merged with population data from ParkServe to calculate per capita values.

### **🔬 Analysis Approach**
- **Independent Variable:** 🌳 **Park size (in acres) per county**
- **Dependent Variables:** 🦠 **COVID-19 confirmed cases and deaths per capita**
- **Filtering Criteria:**
  - Counties with **park sizes greater than 700 acres** and **cases per capita below 0.8** were **excluded** to reduce data skew.
- **Statistical Method Used:**
  - **Ordinary Least Squares (OLS) regression** to estimate correlations between park size and COVID-19 cases.
  - **Logarithmic transformations and outlier removal** were applied to improve model accuracy.

### **📌 Regression Model**
The correlation was estimated using a simple linear regression model:

$Y_C = \beta_1 park_C + \varepsilon$

Where:  
- **Y_C** = Per capita number of confirmed cases or deaths  
- **β₁** = Change in case/death count for a **unit increase in park size**  
- **ε** = Error term  

---

## **Findings & Key Insights**
### **📉 Expected vs. Actual Results**
✔ **Popular Belief:** More green space should mean **cleaner air, better social distancing, and lower COVID-19 cases.**  
❌ **Reality (Findings):** The initial analysis **showed a surprising positive correlation** between **park size and COVID-19 cases** (i.e., more green space didn’t necessarily mean lower infections).  

### **📊 Data Visualizations**
Our study used **geospatial maps and scatter plots** to analyze the trends:

1. **Green Space Distribution:**  
   - A choropleth map showing **park size per county** in mainland U.S.
     ![image](https://github.com/user-attachments/assets/50cae5e9-8299-4da8-a6fc-1b38652dc0fe)

2. **COVID-19 Severity Maps:**  
   - Maps displaying **cumulative COVID-19 cases per county.**
     ![image](https://github.com/user-attachments/assets/07be31cf-34cc-4f9e-acba-0f43deffb151)

3. **Scatter Plots on Park Size vs. Cases:**  
   - **Scatterplot on park size and cases, with full dataset**
   ![image](https://github.com/user-attachments/assets/4a8da5b6-db6a-4cc6-9aad-b62d8b679c3a)
     
   - **Scatterplot on data that has been scaled logarithmically**
     ![image](https://github.com/user-attachments/assets/d012defd-9586-485e-ac70-3eac139ba5a5)

   - **Scatterplot and the best-fitted line on park size and cases**
     ![image](https://github.com/user-attachments/assets/6ed8afcd-f006-4b52-847d-3f469f23bca0)


### **📌 Conclusion**
- **No strong evidence** supports the claim that **more green space directly reduces COVID-19 transmission**.  
- The statistical model **did not yield significant results**, suggesting that other factors **(population density, mobility, socioeconomic variables)** play a larger role.  
- **Urban planning and public health policies should consider multiple factors beyond just green space availability.**

---

## **Further Improvements & Future Research**
🔹 **Expanding Data Scope:** Future studies should incorporate **real-time park usage statistics, air quality data, and public mobility trends** to improve correlation analysis.  
🔹 **Demographic Considerations:** Variables like **population density, age distribution, and income levels** should be factored into the study.  
🔹 **Qualitative Data:** Park quality metrics **(pollution levels, amenities, accessibility, safety perceptions)** should be included for a more holistic understanding.  

---

## **References**
- 📌 **COVID-19 Cases and Deaths:** [USAFacts COVID-19 Tracker](https://usafacts.org/visualizations/coronavirus-covid-19-spread-map/)  
- 📌 **Park Data:** [Trust for Public Land - ParkServe Dataset](https://www.tpl.org/park-data-downloads)  

---
