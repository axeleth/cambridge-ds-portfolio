# Portfolio Description

This repository contains a portfolio of my work from the Cambridge ICE x FourthRev Data Science Career Accelerator. I took on this course to bridge my academic foundations with applied, industry-relevant skills, combining technical training with practical business problem-solving. Over the course of several months, I developed end-to-end solutions to real-world challenges using supervised learning, unsupervised clustering, natural language processing, anomaly detection, and time series forecasting.

This portfolio presents the core projects completed during the programme. Each section outlines the business context, analytical approach, and key learnings. The goal is to demonstrate not only technical proficiency, but also the ability to extract insights, make data-driven decisions, and communicate findings effectively.

---
# Projects

## 🚢 Anomaly Detection in Ship Engine Data

### Project Overview

This project explored how anomalies in ship engine performance metrics can be detected using both statistical and machine learning methods. The goal was to identify early indicators of mechanical issues that may require maintenance. I began with exploratory data analysis to understand the distributions and then applied univariate and multivariate anomaly detection techniques.

### Technical Implementation

After preprocessing and scaling the data, I used dimensionality reduction with PCA to visualize patterns and improve model performance.

Models used:
* IQR Method
* One-class SVM
* Isolation Forest

The IQR method was useful for simple, feature-specific outliers. One-class SVM and Isolation Forest enabled multivariate detection, capturing more complex anomalies. Isolation Forest proved especially effective due to its scalability and interpretability.

### Skills and Capabilities Gained

This project gave me practical experience in unsupervised learning, outlier detection, and dimensionality reduction. I learned to select models based on data complexity and to fine-tune hyperparameters for better control over anomaly thresholds.

**Key Learnings:** Anomaly detection, Unsupervised modeling, One-class SVM, Isolation Forest, PCA, Z-score scaling, Feature-based, multivariate outlier detection

### View Project
[📄 View Report (PDF)](reports/Course_1/Ehrnrooth_Axel_CAM_C101_W5_Mini-project.pdf){:target="_blank"}  
[💻 View Code on GitHub](https://github.com/axeleth/cambridge-ds-portfolio/tree/main/code/Course_1/Ehrnrooth_Axel_CAM_C101_W5_Mini-project.ipynb){:target="_blank"}

---

## 🛍️ Customer Segmentation with K-means Clustering

### Project Overview

This project focused on segmenting customers into meaningful groups using clustering techniques, with the goal of identifying high-value customer profiles and informing business strategy. I engineered new features from raw purchase data to capture behavioral patterns like frequency, recency, and estimated lifetime value. These enriched features allowed for more interpretable and actionable segmentation.

### Technical Implementation

After preprocessing and aggregating the dataset by customer, I engineered five key features and standardized the data to prepare it for clustering. Dimensionality reduction was used to visualize the cluster structures and support interpretation.

Models and methods used:
*	K-means clustering
*	Hierarchical clustering
*	PCA and t-SNE for dimensionality reduction
*	Feature engineering (Age, Recency, Frequency, Unit Cost, CLV)

The optimal number of clusters was selected using both the elbow method and silhouette score, with four clusters offering the best balance of separation and interpretability. t-SNE provided clearer visual distinction of clusters than PCA, especially for non-linear relationships.

### Skills and Capabilities Gained

This project taught me how to create meaningful features from transactional data, tune clustering models for business insights, and visualize high-dimensional data effectively. I also practiced evaluating cluster structures and using segmentation to guide data-driven recommendations.

**Key Learnings:** Customer segmentation, K-means clustering, Dimensionality reduction, Feature engineering, Cluster evaluation

### View Project
[📄 View Report (PDF)](reports/Course_1/Ehrnrooth_Axel_CAM_C101_W6_Mini-project.pdf){:target="_blank"}  
[💻 View Code on GitHub](https://github.com/axeleth/cambridge-ds-portfolio/tree/main/code/Course_1/Ehrnrooth_Axel_CAM_C101_Week_6_Mini-project.ipynb){:target="_blank"}

---

## 🎓 Student Dropout Prediction with Supervised Learning

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

## 💬 NLP Analysis of PureGym Customer Reviews

### Project Overview

In this project, I analyzed customer reviews from PureGym to identify key themes, emotional drivers, and service-related pain points. The goal was to uncover recurring complaints and generate actionable insights that could help improve the member experience across gym locations. Reviews were sourced from Google and Trustpilot, with the analysis focused on low-rated reviews to understand the root causes of dissatisfaction.

### Technical Implementation

The workflow combined traditional NLP tools with advanced transformer-based models and large language models. After preprocessing the reviews (including tokenization, stopword removal, and lowercasing), I used topic modeling and emotion classification to explore both what customers were saying and how they felt.

Techniques used:
*	BERTopic for transformer-based topic modeling
*	Gensim LDA for probabilistic topic discovery
*	Emotion classification using bert-base-uncased-emotion
*	Prompt-based topic extraction and suggestion generation using Falcon-7B-Instruct
*	PCA and t-SNE for topic visualization

BERTopic revealed consistent issues around broken equipment, cleanliness, rude staff, payment problems, and overcrowded facilities. Emotion analysis showed anger as the dominant sentiment in negative reviews, particularly where customer service was involved. Running BERTopic on Falcon-generated summaries allowed deeper insight into root causes and produced focused suggestions for improvement.

### Skills and Capabilities Gained

This project strengthened my ability to preprocess large text datasets, apply and compare multiple NLP models, and interpret unstructured customer feedback at scale. I learned to use emotion classifiers and language models to go beyond surface-level complaints and support data-driven recommendations for customer experience improvement.

**Key Learnings:** Natural language processing, Topic modeling (BERTopic, LDA), Emotion analysis with BERT, Prompt engineering with LLMs, Text cleaning and preprocessing, Customer insight extraction

### View Project
[📄 View Report (PDF)](reports/Course_3/Ehrnrooth_Axel_CAM_C301_Week_4and5_Topic_project.pdf){:target="_blank"}  
[💻 View Code on GitHub](https://github.com/axeleth/cambridge-ds-portfolio/tree/main/code/Course_3/Ehrnrooth_Axel_CAM_C301_Week_4and5_Topic_project.ipynb){:target="_blank"}

---

## 📚 Book Sales Forecasting with Time Series Models

### Project Overview

This project focused on forecasting book sales using weekly and monthly historical sales data from Nielsen BookScan. The objective was to support independent publishers in making informed stock and reprint decisions by modeling both short-term trends and long-term seasonal demand. I applied and compared two modeling approaches: a statistical time series model and a supervised machine learning model.

### Technical Implementation

The dataset included weekly sales data for 500 books, with two titles selected for focused analysis: The Very Hungry Caterpillar and The Alchemist. After preprocessing and filling missing weeks, I performed trend and seasonality decomposition, autocorrelation analysis, and stationarity testing to guide model choice and tuning.

Models used:
*	Auto ARIMA
*	XGBoost with lagged features

Auto ARIMA effectively captured seasonal sales spikes, especially year-end surges, in both weekly and monthly data. XGBoost, using a tuned lag window and cross-validation, performed better on the weekly data by modeling finer short-term fluctuations, but it struggled with seasonal peaks in monthly forecasts.

### Skills and Capabilities Gained

This project helped me understand how different modeling techniques perform across time resolutions. I learned how to prepare time series data for both statistical and machine learning methods, tune lag-based models, apply cross-validation strategies for temporal data, and evaluate forecast accuracy with MAE and MAPE.

**Key Learnings:** Time series forecasting, Auto ARIMA modeling, Lag-based machine learning, STL decomposition, ACF and PACF interpretation, Stationarity testing, Expanding window cross-validation, Sales demand modeling

### View Project
[📄 View Report (PDF)](reports/Course_3/Ehrnrooth_Axel_CAM_C301_Week_9&10_Topic_project.pdf){:target="_blank"}  
[💻 View Code on GitHub](https://github.com/axeleth/cambridge-ds-portfolio/tree/main/code/Course_3/Ehrnrooth_Axel_CAM_C301_Week_9&10_Topic_project.ipynb){:target="_blank"}

---

# 🏦 NLP of G-SIB Earnings Calls for the Bank of England

### Project Overview

This capstone project represented the final stage of the Cambridge Data Science Career Accelerator and was conducted in collaboration with the Bank of England’s Prudential Regulation Authority. It provided our team with a unique opportunity to act as independent data scientists and design our own solution to a real-world regulatory challenge. We were asked to determine whether unstructured data from quarterly earnings call transcripts of global systemically important banks could be used to identify early indicators of financial risk, strategic shifts, or emerging market concerns.

The problem required us to combine creativity, domain understanding, and technical skill. Rather than working from a fixed brief, we had full responsibility for designing and delivering a solution that could support supervisory judgment in a high-stakes regulatory context.

### Technical Implementation

We built a modular natural language processing pipeline that could process, analyze, and interpret long-form transcripts. The pipeline integrated several analytical components that each addressed a different aspect of the broader risk-monitoring task.

Techniques and models used:
* FinBERT for risk-based sentiment classification
* DeBERTa-v3 for aspect-based sentiment analysis
* BERTopic and GPT-4.1 for topic modeling and summarisation
* Gemini Flash for question avoidance detection
* LangChain and a vector database for retrieval-augmented generation

Our analysis included transcripts from Citibank, JPMorgan, and UBS, spanning over a decade. We also used Silicon Valley Bank as a benchmark for identifying risk-related language in failed institutions. To forecast risk levels over time, we developed a hybrid time series model that combined SARIMA with XGBoost and applied it to trends in high-risk sentiment.

The analysis consistently surfaced major concerns including exposure to commercial real estate, net interest margin pressure, capital adequacy, and cybersecurity. Sentiment toward loan book quality was more often negative than positive. UBS and JPMorgan emerged as banks showing either elevated or volatile high-risk language across recent quarters.

### My Role

As team lead, I focused on coordinating planning, facilitating discussion, and supporting team-wide communication. I helped align each technical component with the project’s core objectives and ensured that all team members contributed meaningfully across the different modules. I also contributed directly to refining the structure of our analytical pipeline, helping maintain a clear and consistent vision for the project from beginning to end.

Taking on this role pushed me to grow as both a communicator and a decision-maker. I learned to balance individual initiative with group input and to keep our momentum going even when the project became technically complex.

### Skills and Capabilities Gained

This project deepened my understanding of applied NLP and strengthened my ability to manage multi-part analytical workflows. I became more confident in tuning and deploying large language models, interpreting financial sentiment, and building tools that transform technical insight into decision-making support. Leading a team in this context gave me valuable experience in shaping project structure, resolving roadblocks, and presenting work to a professional audience.

### Key Learnings

* Natural language processing for financial supervision
* Sentiment classification and aspect modeling
* Topic extraction using BERTopic and LLMs
* Question avoidance detection with large language models
* Time series forecasting with SARIMA and XGBoost
* Retrieval-augmented generation using LangChain
* Semantic search and document chunking
* Collaborative leadership in applied data science

[📄 View Report (PDF)](reports/Bank_of_England_Project/STOMPA_CAM_EP_Assignment3_report.pdf){:target="_blank"}  
[💻 View Code in Google Drive](https://colab.research.google.com/drive/1HF6FiC_HcfOiSa7C8VaR6xbk9dkLPhYB?usp=sharing){:target="_blank"}

