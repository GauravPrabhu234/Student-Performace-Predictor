# Student-Performace-Predictor

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data_Analysis-150458?logo=pandas)
![NumPy](https://img.shields.io/badge/NumPy-Numerical_Computing-013243?logo=numpy)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557c)
![Seaborn](https://img.shields.io/badge/Seaborn-Statistical_Visualization-4c72b0)
![Project](https://img.shields.io/badge/Project-EDA-success)

## Project Overview

This project focuses on performing Exploratory Data Analysis (EDA) on a Student Performance in Exams dataset to understand students' academic performance and identify patterns, trends and relationships among different variables.

The analysis explores how students' Maths, Reading and Writing scores vary across demographic and educational categories such as gender, race/ethnicity, parental education level, lunch category and test preparation course completion.

The project uses Python-based data analysis and statistical techniques to extract meaningful insights from the dataset.

## Business Problem

Understanding student academic performance is important for identifying patterns and potential factors associated with educational outcomes.

This project investigates the following questions:

- How do students perform across Maths, Reading and Writing?
- Are there differences in academic performance between male and female students?
- How does performance vary across different lunch categories?
- Is test preparation course completion associated with higher examination scores?
- How does parental education level relate to students' academic performance?
- What relationships exist between the three examination subjects?

## Project Objectives

- Understand the dataset structure and variables.
- Inspect and assess data quality.
- Identify missing values, duplicate records and potential outliers.
- Perform univariate and bivariate analysis.
- Apply descriptive statistics and statistical hypothesis testing.
- Visualize distributions and relationships between variables.
- Identify meaningful patterns and summarize key findings.

## Dataset Description

The dataset contains **1,000 student records and 8 columns**.

| Column | Description | Data Type |
|---|---|---|
| gender | Gender of the student | Categorical |
| race/ethnicity | Student's race/ethnicity group | Categorical |
| parental level of education | Parent's highest education level | Categorical |
| lunch | Lunch category | Categorical |
| test preparation course | Test preparation completion status | Categorical |
| math score | Maths examination score | Numerical |
| reading score | Reading examination score | Numerical |
| writing score | Writing examination score | Numerical |

**Dataset source:** Add the original Kaggle dataset URL here.

## Technologies and Libraries

The project uses the following tools and Python libraries:

- **Python:** Core programming language.
- **Pandas:** Data manipulation and analysis.
- **NumPy:** Numerical computations.
- **Matplotlib:** Data visualization.
- **Seaborn:** Statistical visualization.
- **SciPy:** Statistical hypothesis testing.
- **Statsmodels:** Multiple comparison testing using Tukey HSD.
- **Jupyter Notebook:** Interactive analysis environment.

## Project Workflow

### 1. Introduction and Problem Understanding
Defined the project objective, business problem and analysis goals.

### 2. Data Loading and Understanding
- Imported required libraries.
- Loaded the dataset.
- Examined dataset dimensions, columns and data types.
- Reviewed numerical and categorical variables.

### 3. Data Cleaning
- Checked missing values.
- Checked duplicate records.
- Investigated potential outliers using the IQR method.
- Retained observations where there was no sufficient evidence that they were invalid.

### 4. Exploratory Data Analysis

**Univariate Analysis**
- Numerical analysis using mean, median, variance, standard deviation, quartiles and skewness.
- Categorical analysis using frequency, relative frequency and mode.

**Bivariate Analysis**
- Compared academic scores across gender, lunch, test preparation, parental education and race/ethnicity categories.
- Examined correlations between Maths, Reading and Writing scores.

**Statistical Analysis**
- Welch's Independent Samples t-test.
- Cohen's d effect size.
- One-way ANOVA.
- Tukey's HSD post-hoc test.

### 5. Data Visualization

The following visualizations were created:

- Histograms for numerical score distributions.
- Count plots for categorical variables.
- Box plots for comparing score distributions across categories.
- Scatter plots for relationships between numerical variables.
- Correlation heatmap for numerical score relationships.

### 6. Key Findings and Conclusion
Summarized the major statistical observations, relationships and findings from the analysis.

## Key Findings

### 1. Overall Academic Performance

| Subject | Average Score |
|---|---:|
| Maths | 66.09 |
| Reading | 69.17 |
| Writing | 68.05 |

Reading had the highest average score, followed by Writing and Maths.

### 2. Gender and Academic Performance

- Male students had a higher average Maths score.
- Female students had higher average Reading and Writing scores.
- The largest average difference was observed in Writing.

### 3. Lunch Category

Students in the Standard lunch category had higher average scores across all three subjects compared with students in the Free/reduced category.

### 4. Test Preparation

Students who completed the test preparation course had higher average scores in Maths, Reading and Writing than students who did not complete it.

### 5. Parental Education

Students in the Master's degree parental education category had the highest average scores across all three subjects, while the High school category had the lowest average scores.

### 6. Correlation Analysis

| Subject Pair | Correlation |
|---|---:|
| Maths – Reading | 0.818 |
| Maths – Writing | 0.803 |
| Reading – Writing | 0.955 |

Reading and Writing demonstrated the strongest positive correlation.

## Statistical Analysis Results

### Welch's Independent Samples t-test

**Comparison:** Gender vs Maths Scores

| Metric | Result |
|---|---:|
| T-statistic | -5.3980 |
| P-value | 8.4208 × 10⁻⁸ |
| Cohen's d | -0.3407 |
| Effect size | Small |

The test identified a statistically significant difference in mean Maths scores between male and female students. The standardized effect size was small.

### One-Way ANOVA

**Comparison:** Parental Education vs Maths Scores

| Metric | Result |
|---|---:|
| F-statistic | 6.5216 |
| P-value | 5.5923 × 10⁻⁶ |
| Significance level | 0.05 |

The result indicated statistically significant differences in mean Maths scores among at least some parental education categories.

### Tukey's HSD

Out of 15 pairwise comparisons, 6 showed statistically significant differences at the 0.05 significance level.

The results identified differences involving the High school, Associate's degree, Bachelor's degree, Master's degree and Some college categories.

**Note:** These statistical findings indicate associations and differences, not causal relationships.

## Project Structure

```text
Student-Performance-EDA/
│
├── Student_Performance_EDA.ipynb
│
├── README.md
│
└── data/
    └── StudentsPerformance.csv
```

*Adjust the filenames and folder structure to match your actual repository.*

## How to Run the Project

### Prerequisites

- Python 3.x
- Jupyter Notebook
- Required Python libraries

### 1. Clone the Repository

```bash
git clone https://github.com/GauravPrabhu234/Student-Performace-Predictor.git
```

### 2. Navigate to the Project Directory

```bash
cd Student-Performance-EDA
```

### 3. Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn scipy statsmodels jupyter
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

### 5. Open the Notebook

Open `Student_Performance_EDA.ipynb` and run the notebook cells sequentially.

Ensure the dataset is placed in the correct directory before executing the notebook.

## Limitations

- The dataset contains limited information about students and their academic backgrounds.
- The analysis is observational and cannot establish causal relationships.
- Race/ethnicity categories are anonymized.
- Statistical tests were performed on selected comparisons rather than every possible relationship.
- Findings may not generalize to all student populations.

## Future Improvements

- Develop a Machine Learning model to predict student examination scores.
- Perform feature engineering and feature importance analysis.
- Explore additional statistical tests and model evaluation techniques.
- Investigate predictive relationships between student characteristics and academic performance.

## Conclusion

This project demonstrates the application of Exploratory Data Analysis to investigate student academic performance using Python.

Through data cleaning, statistical analysis and visualization, meaningful patterns and relationships were identified across examination scores and student categories.

The project provides practical experience in data analysis, statistical reasoning, hypothesis testing and visualization, while establishing a foundation for future Machine Learning projects.

---

**Project Category:** Exploratory Data Analysis (EDA)  
**Domain:** Education / Academic Performance  
**Tools:** Python, Pandas, NumPy, Matplotlib, Seaborn, SciPy, Statsmodels  
**Status:** EDA Analysis Completed
