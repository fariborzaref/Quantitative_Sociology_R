# Quantitative Sociology with R  
**Instructor:** Dr. Fariborz Aref  

---

### Overview
This repository accompanies the course **Quantitative Sociology with R**, a graduate and upper-undergraduate course designed to integrate sociological theory with rigorous statistical modeling.  
Students move from conceptualizing inequality and structure to producing fully reproducible R analyses and reports.

---

### Course Objectives
- Translate sociological questions into measurable variables and models.  
- Master regression, GLM, GEE, HLM, and SEM using real-world social data.  
- Apply visualization and interpretation techniques that communicate evidence clearly.  
- Build reproducible pipelines using **R Markdown / Quarto**, `tidyverse`, and GitHub.  
- Develop critical reasoning about data, bias, and theory.

---

### Core Topics by Module
| Week | Theme | Core Focus |
|------|--------|-------------|
| **1** | Foundations of Sociological Data | Tidy data, measurement, and validity |
| **2** | Descriptive Inequality | Distributions, Lorenz & Gini, visual storytelling |
| **3** | Regression Logic | Model specification, interpretation, and causality |
| **4** | Generalized Linear Models | Binary and count outcomes in social data |
| **5** | Hierarchical & Longitudinal Models | Individuals nested in contexts; HLM vs. GEE |
| **6** | Structural Equation Models | Latent constructs, path diagrams, mediation |
| **7** | Visualization & Reporting | `ggplot2`, marginal effects, coefficient plots |
| **8** | Replication & Open Science | Transparency, Quarto, GitHub publishing |

---

### Key R Packages
```r
# Core workflow
library(tidyverse)
library(broom)
library(ggplot2)
library(performance)

# Modeling
library(lme4)          # Hierarchical / Multilevel models
library(geepack)       # Generalized Estimating Equations
library(lavaan)        # Structural Equation Modeling
library(fixest)        # Econometric fixed-effects
library(marginaleffects)  # Marginal predictions & plots

# Output and reproducibility
library(modelsummary)
library(quarto)
library(lme4)
model <- lmer(inequality ~ education + income + (1 + income | country), data = oecd_panel)
summary(model)
performance::icc(model)
Quantitative_Sociology_R/
├── Week01_Data/
│   ├── data_intro.R
│   └── survey_clean.csv
├── Week02_Descriptive/
├── Week03_Regression/
├── Week04_GLM/
├── Week05_HLM_GEE/
├── Week06_SEM/
├── Week07_Visualization/
├── Week08_OpenScience/
└── Project_Replication/
