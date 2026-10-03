# Sleep Health and Lifestyle Data Analysis

Exploratory data analysis (EDA) of how lifestyle and health factors relate to sleep quality and sleep disorders, using Python.

## Objective

Find out which factors (stress, BMI, occupation, gender, age, physical activity, blood pressure, heart rate and daily steps) are linked to **sleep quality, sleep duration and sleep disorders** (Insomnia and Sleep Apnea).

## Dataset

- Source: [Sleep Health and Lifestyle Dataset (Kaggle)](https://www.kaggle.com/datasets/uom190346a/sleep-health-and-lifestyle-dataset)
- 374 records, 13 columns
- Sleep disorder labels: None (219), Sleep Apnea (78), Insomnia (77)
- Columns include: Gender, Age, Occupation, Sleep Duration, Quality of Sleep, Physical Activity Level, Stress Level, BMI Category, Blood Pressure, Heart Rate, Daily Steps, Sleep Disorder

## Tools Used

Python, Pandas, Matplotlib, Seaborn, Jupyter Notebook

## Approach

1. Loaded the data and checked structure, summary statistics and missing values
2. Cleaned the data (kept "None" as a valid sleep disorder category, merged duplicate BMI labels)
3. Created 25 visualizations: count plots, bar plots, box plots, violin plot, histograms, scatter plots, correlation heatmap, pair plot and pie charts
4. Compared lifestyle and health variables across sleep disorder groups
5. Summarized the results in a presentation

## Key Findings

- **Stress is the strongest factor.** Stress level has a strong negative correlation with quality of sleep (r ≈ -0.90) and sleep duration (r ≈ -0.81). Sleep duration and quality are strongly positively related (r ≈ 0.88).
- **Sleep quality by group.** Average quality of sleep is lowest for Insomnia (6.5), then Sleep Apnea (7.2), and highest for people with no disorder (7.6). Average stress is highest in the Insomnia group (5.9) and lowest in the no-disorder group (5.1).
- **BMI.** Most Insomnia and Sleep Apnea cases are in the Overweight category (64 and 65 cases).
- **Occupation.** Nurses account for most Sleep Apnea cases (61), while Salespersons and Teachers account for most Insomnia cases (29 and 27).
- **Gender.** Sleep Apnea is far more common among women than men in this dataset (67 vs 11). Insomnia counts are similar (41 male, 36 female).
- **Age.** Sleep Apnea records are older on average (about 50 years) than the no-disorder group (about 39).
- **Blood pressure.** A reading of 140/95 appears mostly in Sleep Apnea records (59 of 65).
- **Physical activity.** Sleep Apnea records show the highest activity level and Insomnia the lowest. This is unexpected and worth investigating further.

## Limitations

- The dataset is small (374 records) and appears to be synthetic, so results show association, **not causation**, and may not generalize to real populations.
- Many rows are near-identical apart from Person ID, which can inflate some patterns.
- Some groups (for example, some occupations) have very few records.

## Repository Structure

```
.
├── data/
│   └── Sleep_health_and_lifestyle_dataset.csv
├── notebook/
│   └── sleep_health_analysis.ipynb
├── presentation/
│   └── Sleep_Data_Analysis_Presentation.pptx
└── README.md
```

## How to Run

```bash
git clone https://github.com/rujal7/Sleep-Health-and-Lifestyle.git
cd Sleep-Health-and-Lifestyle
pip install pandas matplotlib seaborn jupyter
jupyter notebook notebook/sleep_health_analysis.ipynb
```

If you keep the CSV in the same folder as the notebook, no path change is needed. Otherwise update the path in the load cell.

## Possible Next Steps

- Build a classification model to predict sleep disorder (for example, logistic regression or random forest) and evaluate it with precision, recall and F1-score
- Split blood pressure into systolic and diastolic values for numeric analysis
- Build an interactive dashboard (Streamlit or Power BI)

## Author

**Rajneesh Sharma**
[GitHub](https://github.com/rujal7)
