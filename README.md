# Portfolio Description

This repository contains a portfolio of all my work from the Cambridge ICE x FourthREV Data Science career accelerator. It is divided into five sections, one for each of the projects I have carried out. I will describe the project, the business problem, the challenges faced, and what I learned.

---
# Projects

## 🎓 Dropout Prediction Project

### Overview

This project focused on identifying students at risk of dropping out at three distinct stages of their academic journey: early registration, mid-course, and late-stage performance. The objective was to support early interventions by building predictive models that could flag at-risk students based on progressively richer data. Starting with basic demographic and course information, I later introduced attendance records and academic performance metrics to evaluate how model accuracy evolved as more meaningful data became available.

### Insights and Outcomes

The stepwise design of the project helped me understand how prediction quality improves with each new layer of information. Early-stage models, built on limited demographic data, offered only a general sense of risk. By mid-course, the inclusion of attendance patterns provided behavioral context and modestly improved performance. It was in the final stage, when academic outcomes were introduced, that the models achieved the highest levels of accuracy and recall. This clearly showed that timely academic data holds the strongest predictive value for understanding student outcomes.

### Technical Implementation

On the technical side, I developed a complete supervised learning pipeline using two complementary modeling approaches.

Models used:
* XGBoost
* Neural Network (Keras)

XGBoost was optimized through grid search, while the neural network benefited from Bayesian hyperparameter tuning. I applied feature embeddings to manage high-cardinality categorical features such as course name and nationality, which helped maintain performance and avoid dimensionality issues. Each model was evaluated using multiple metrics including F1-score, precision, recall, accuracy, and AUC, with AUC proving especially useful in addressing the imbalanced nature of the dataset.

### Challenges and Solutions

I also addressed practical challenges such as over-reliance on a single academic feature by creating a normalized academic success indicator. This improved the interpretability and robustness of the final model. Through feature importance analysis and iterative model tuning, I developed a deeper understanding of how to balance model performance with fairness and generalizability.

### Skills and Capabilities Gained

From this project, I gained the ability to design, implement, and evaluate multi-phase predictive pipelines. I became comfortable tuning complex models for different stages of data availability, managing categorical encoding through embeddings, and interpreting model behavior in the context of real-world decisions. Most importantly, I learned how machine learning can be used not just for classification, but for timely, actionable insight in high-impact areas like education.

**Key Learnings:** Feature engineering, supervised learning, model tuning (grid and Bayesian), feature embeddings, multi-stage pipeline design, imbalanced data handling, evaluation metrics, feature importance analysis

### View Project
[📄 View Report (PDF)](reports/Course_2/Ehrnrooth_Axel_CAM_C201_W6_Mini-project.pdf){:target="_blank"}  
[💻 View Code on GitHub](https://github.com/axeleth/cambridge-ds-portfolio/tree/main/code/Course_2/Ehrnrooth_Axel_CAM_C201_Week_6_Mini-project.ipynb){:target="_blank"}

---
