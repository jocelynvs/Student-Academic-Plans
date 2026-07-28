# Student Segmentation for Academic Planning using K-Modes Clustering

This project was developed for the **Data Analysis Competition (DAC) Informatics Festival 2022**, hosted by **Universitas Padjadjaran (UNPAD)**. The objective was to analyze student characteristics and identify distinct student groups that can be used to support more targeted academic guidance and intervention strategies.

Unlike predictive models that require labeled outcomes, this project applies **unsupervised machine learning** to discover hidden patterns among students based on their demographic, academic, and behavioral characteristics.

---

## Problem Statement

Higher education institutions often provide the same academic guidance to all students despite having students with diverse backgrounds, learning behaviors, and academic performance.

This project aims to answer the following questions:

- Can students be grouped according to their academic characteristics?
- What distinguishes each student group?
- How can these groups be utilized to design more personalized academic planning and support?

The resulting clusters can assist universities in developing data-driven academic policies, student mentoring programs, and intervention strategies.

---

## Dataset

**Source:** Data Analysis Competition (DAC) Informatics Festival 2022, Universitas Padjadjaran

The dataset contains anonymized student information, including:

- Gender
- Student status
- Residence
- GPA
- Academic performance
- Organizational involvement
- Scholarship status
- Other demographic and educational attributes

---

## Methodology

### 1. Data Understanding

The project began by exploring the dataset to understand the available student attributes, data types, variable distributions, and missing values. This step helped identify the characteristics of the data before applying any machine learning techniques.

### 2. Data Cleaning

The dataset was cleaned by removing missing records, duplicate entries, and variables that were not relevant for clustering. These preprocessing steps help improve cluster quality and reduce unnecessary noise.

### 3. Data Preprocessing

Because the dataset consists primarily of categorical variables, the data were encoded into numerical representations suitable for K-Modes clustering while preserving their categorical nature.

### 4. Student Segmentation using K-Modes

K-Modes clustering was selected because it is specifically designed for categorical datasets, unlike K-Means which relies on numerical distance calculations.

Several values of **k** were evaluated, and the optimal number of clusters was determined using:
- Elbow Method
- Calinski-Harabasz Index

The final clustering model was then trained using the selected number of clusters.

### 5. Cluster Interpretation

After clustering, each student group was profiled by comparing the distribution of demographic, academic, and extracurricular variables. Visualizations were used to identify the defining characteristics of each cluster and translate the results into actionable academic insights.

---

## Insights Obtained

The K-Modes clustering analysis identified **four distinct student profiles**, each representing different academic and extracurricular characteristics. These findings demonstrate that students have diverse needs and may benefit from different academic support strategies.

* **Cluster 1 – Academically Outstanding Students**

  * High academic achievers with excellent GPA.
  * Many students are actively involved in student organizations while maintaining strong academic performance.
  * This group has strong potential for leadership development and academic excellence programs.

* **Cluster 2 – High-Achieving Scholarship Students**

  * Students with consistently good academic performance and a high proportion of scholarship recipients.
  * Demonstrate strong academic commitment and learning motivation.
  * Suitable candidates for advanced academic opportunities and scholarship development programs.

* **Cluster 3 – Students Requiring Academic Support**

  * Characterized by moderate academic performance and relatively lower extracurricular participation.
  * May benefit from academic mentoring, study skill improvement, and personalized guidance to enhance their academic outcomes.

* **Cluster 4 – Diverse Student Population**

  * The largest and most heterogeneous cluster, consisting of students with varied academic and demographic characteristics.
  * Highlights that not all students fit into a single profile, emphasizing the importance of personalized academic planning rather than one-size-fits-all interventions.

Overall, the clustering results demonstrate that unsupervised learning can effectively uncover meaningful student profiles from categorical educational data. These insights can support universities in designing **more targeted academic advising, mentoring programs, scholarship strategies, and student support initiatives** based on the characteristics of each student group.

---

## Tools Used

- Python
- Pandas
- NumPy
- Scikit-learn
- KModes
- Matplotlib
- Seaborn

---

## Skills Demonstrated

- Exploratory Data Analysis (EDA)
- Data Cleaning
- Feature Engineering
- Categorical Data Processing
- Unsupervised Machine Learning
- K-Modes Clustering
- Cluster Evaluation
- Data Visualization
- Insight Generation

---

## Repository Structure

```
.
├── dataset.csv                 # Student dataset used for clustering analysis
├── notebook.ipynb              # Complete implementation including EDA, preprocessing, K-Modes clustering, evaluation, and visualization
├── Rencana_Akademik_Paper.pdf  # Research paper describing the methodology, experiments, and findings
└── README.md                   # Project documentation and overview
```

The repository includes the implementation notebook and the accompanying project paper, which provides a detailed explanation of the methodology, clustering process, evaluation, and interpretation of the results.
