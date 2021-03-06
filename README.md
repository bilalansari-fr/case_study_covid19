<!-- Add banner here -->
![Banner](https://sfc.asso.fr/wp-content/uploads/2020/03/Covid.jpg)

# Case Study: COVID-19

<!-- Add buttons here -->


![GitHub last commit](https://img.shields.io/github/last-commit/bilalsp/case_study_covid19)
![GitHub pull requests](https://img.shields.io/github/issues-pr/bilalsp/case_study_covid19)
![GitHub issues](https://img.shields.io/github/issues-raw/bilalsp/case_study_covid19)
![GitHub stars](https://img.shields.io/github/stars/bilalsp/case_study_covid19)


<!-- Describe your project in brief -->
In this case study on COVID-19, we perform statistical test (ANOVA) to examine the statistical significance of number of confirmed cases and fatality cases across the different regions in the world. 

# Table of contents
- [Description](#Description)
- [Hypothesis Formulation](#hypothesis-formulation)
- [Data Preparation](#data-preparation)
- [Experimental Design](#experimental-design)
- [Conclusion](#Conclusion)

## Description
We explore the COVID-19 data consisting of confirmed, deaths, recovered, and active cases from all around the world. First, we formulate the hypothesis for our study based on that we design our experiment. One-way ANOVA statistical test fit for our case study but, we observed that raw data violate the normality assumption. So, we apply log transformation to reduce the outlier effect. Different methods like the Q-Q plot, Shapiro-Wilk test are used to test the normality of data. After ANOVA analysis, the Tukey HSD method is used for further investigation.

## Hypothesis Formulation
We want to investigate that **is there any 
statistical difference in the number of COVID-19 confirmed cases and fatality cases across the different regions in the world?** If difference exists, we further identify the pair of regions where the difference lies. 
To answer the above question statistically, we formulate following two case studies. 

**Case Study-1: COVID-19 (Confirmed Cases)**

<img src="https://render.githubusercontent.com/render/math?math=H_0:"> There is no statistical difference in the mean of COVID-19 confirmed cases across the different regions. <br>
<img src="https://render.githubusercontent.com/render/math?math=H_1:"> At least the means of COVID-19 confirmed cases of two regions are different from each other.

**Case Study-2: COVID-19 (Fatality Cases)**
<img src="https://render.githubusercontent.com/render/math?math=H_0:">There is no statistical difference in the mean of COVID-19 fatality cases across the different regions. <br>
<img src="https://render.githubusercontent.com/render/math?math=H_1:"> At least the means of COVID-19 fatality cases of two regions are different from each other.

## Data Preparation
Data has been collected on 10th May 2020 from Johns Hopkins University. We manipulate raw data of COVID-19 as per the requirement of our case study. We decided to categories the countries into following four different regions based on the continents. 
```
AFRO: Africa
AMER: North America and South America
EURO: Europe
OCEA: Asia and Oceania
```
Consider the 20 countries from each regions for case studies.

Data Source:  [COVID-19 Data Repository by JHU](https://github.com/CSSEGISandData/COVID-19)

Follow notebook [data_preparation](data_preparation.ipynb)

## Experimental Design
After understanding the problem statement and hypothesis formulation, we decide to use the one-way analysis of variance (ANOVA) to determine whether there is any statistically significant difference between the means of COVID-19 confirmed cases and fatality cases of two or more regions. One-way ANOVA is used because we have only one independent variable(i.e., region) and sample data from each region is independent from others.

###### Case Study-1
```
Dependent Variable: number of confirmed cases 
Independent Variable: region
```
Follow notebook [confirmed_cases](confirmed_cases.ipynb) 
###### Case Study-2
```
Dependent Variable: number of fatality cases 
Independent Variable: region
```
Follow notebook [fatality_cases](fatality_cases.ipynb) 

## Conclusion
Statistical analysis has been conducted to establish the statistical significance of COVID-19 cases across the different regions. We analyze the ANOVA result of both case studies and observed that there is a statistically significant difference in means of COVID-19 confirmed cases and fatality cases across the different regions. For further investigation where the difference exists, we used the Tukey HSD test and observed that **mean of COVID-19 confirmed cases and fatality cases for the AFRO region is statistically different from other regions AMR, EURO, and OCEA at 0.05% significance level. It might be because of low testing capacity resulting from few testing equipment in Africa and due to data gap governments in African countries don’t register deaths properly**. 

## References

- Ostertagová, E. and O. Ostertag. “Methodology and Application of One-way ANOVA.” (2013).
- Sam, Shem Otoi. “Exploring the statistical significance of Africa covid-19 data.” (2020). International Journal of Applied Mathematics and Statistics.

