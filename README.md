# 📄 Resume Ranking & Candidate Shortlisting System 🤖✨

## 🧠 Project Overview
This project builds an intelligent system that automates the **ranking of resumes** and **shortlisting of candidates** based on how well they match job requirements. Using **natural language processing (NLP)** and **machine learning**, it saves recruiters from sifting through mountains of resumes manually.

## ❓ Problem Statement
Manually reviewing thousands of resumes is **slow, subjective**, and often **inconsistent**. This system automates the process by:
- Analyzing candidate resumes
- Extracting and combining critical attributes
- Ranking candidates based on **relevance score** (`matched_score`)

## 🎯 Objectives
- Automate resume evaluation using ML.
- Extract and process resume text for analysis.
- Predict match scores using TF-IDF and regression models.
- Visualize top skills and feature importance.

## 🗃️ Dataset
- **Total Entries**: 9544 resumes
- **Columns (22)**: Include `skills`, `degree_names`, `educational_institution_name`, `experience_requirement`, etc.
- **Target**: `matched_score` – A numerical value indicating how well a resume matches a job.

## 🛠️ Tech Stack & Libraries
- **Language**: Python 🐍
- **Libraries**: `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`, `re`, `WordCloud`
- **ML Model**: `RandomForestRegressor`

## 🧹 Data Preprocessing
- Removed columns with >50% missing values
- Filled nulls with empty strings
- Combined key text columns into one (`skills`, `degrees`, `responsibilities`, etc.)
- Cleaned text (lowercasing, punctuation/digit removal)
- Handled outliers in `matched_score` using IQR

## 🔍 Feature Engineering
- Parsed stringified skills to actual Python lists
- Generated a frequency bar plot of top 20 skills
- Created a WordCloud of common skills

## 🧪 Feature Extraction
- Used **TF-IDF vectorization** to transform resume text into numerical features
- Capped at **5000 most relevant features**

## 🎓 Model Training & Evaluation
- **Model**: `RandomForestRegressor` with 150 trees
- **Train/Test Split**: 80/20
- **Performance**:
  - 🔻 MSE: `0.0116`
  - 📈 R² Score: `0.568`

## 📊 Visualizations
- Histogram of match scores
- Scatter plot: Experience vs Match Score
- Actual vs Predicted Match Scores
- Bar chart: Top 20 most important words (TF-IDF features)

## 💡 Future Improvements
- Integrate with ATS (Applicant Tracking Systems)
- Use Deep Learning models like BERT for semantic matching
- Enable real-time resume ranking from uploaded PDFs
