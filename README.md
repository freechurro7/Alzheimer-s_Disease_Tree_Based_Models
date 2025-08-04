# Alzheimer-s_Disease_Tree_Based_Models
This project explores the application of machine learning, particularly tree-based classification models, to predict Alzheimer's Disease diagnosis among the elderly. Thus initiative seeks to humanize data science by understanding cognitive decline and its implications through various lenses

# Project Motivation

Old age brings wisdom, but also vulnerability - particularly cognitive and functional decline. Alzheimer’s Disease (AD), the most common cause of dementia, impairs memory, behavior, and daily functionality. This project began as a personal curiosity but grew into a deeper investigation: 
- Can data science shed light on the invisible deterioration of the mind?
- Can we build robust models to assist in early diagnosis?
- What features or lifestyle factors might hold predictive power?
- How important is standardized testing in clinical research for assessing cognitive and functional abilitiea and how inclusive are these tests across every demographic?

# Description

This analysis is built upon a dataset comprising 2,149 patients, each with 35 features that offer a peek into their demographic details, medical histories, cognitive test scores, and daily functionality.

- Demographics: age, gender, ethnicity, education
- Lifestyle choices: physical activity, alcohol consumption, diet, sleep, and BMI
- Medical history: chronic conditions like diabetes, hypertension, cardiovascular disease, and past head injuries
- Cognitive and functional assessments: MMSE (Mini Mental State Examination), ADL (Activities of Daily Living), and FAST (Functional Assessment Staging Tool)
- Symptoms: forgetfulness, disorientation, confusion, task difficulty, personality changes
- Diagnosis: a binary label — does this individual have Alzheimer’s?

Importantly, the dataset was clean — no missing values, no duplicates.

# EDA
So, before rushing to models, I spent time getting to know the data intimately. What patterns emerge with age? Do lifestyle choices impact diagnosis? Are there symptoms that sharply separate those with Alzheimer’s from those without? These questions guided my exploration.

The initial glimpse at that the dataset had more negative diagnoses than positive (roughly 65% vs. 35%), it wasn’t overly imbalanced. That allowed for clean modeling without resorting to heavy rebalancing techniques.

The cognitive assessment scores (MMSE, ADL, and FAST) — quickly emerged as the most distinguishable factors for Alzheimer's. Patients with lower scores in these areas consistently aligned with positive Alzheimer’s diagnoses. Interestingly, MMSE scores varied with education. Patients with no formal education scored significantly lower than those with high school or tertiary education. However, when examining other assessments like FAST and ADL, educational differences disappeared. This raised a subtle but important flag: cognitive testing must be inclusive and considerate of socioeconomic and educational background

Contrary to common assumptions, factors like BMI, cholesterol, alcohol consumption, and even family history of Alzheimer’s did not show strong predictive patterns. After running null-hypothesis tests, It was surprising to realize that what we often consider “risk factors” in popular discourse were not as statistically meaningful here.

However, a few conditions stood out. Patients with cardiovascular diseases, head injuries, and hypertension had slightly higher positive diagnoses. The presence of behavioral problems and memory complaints proved to be some of the most reliable non-cognitive predictors of Alzheimer's.

# Machine Learning

With the characters introduced and their behaviors understood, I transitioned into modeling. I selected several tree-based classifiers known for their interpretability and robustness, including Decision Tree, Random Forest, Gradient Boosting, and XGBoost, while Logistic Regression served as a baseline.

The tree-based models performed exceptionally well, with Random Forest and XGBoost achieving high accuracy and recall scores. But more importantly, the feature importance results validated what was observed in EDA: MMSE, ADL, and FAST were the top features. Behavioral and memory-related symptoms followed closely. Lifestyle and vital stats played a far smaller role. This alignment between data exploration and model output built confidence in the results.

# Takeaways

- Cognitive and functional scores should be routinely measured in geriatric care — they are early warning signals of Alzheimer’s.
- Behavioral shifts and memory complaints should be taken seriously, even in the absence of other symptoms.
- Education-sensitive cognitive testing tools should be developed to ensure fair assessment across different populations.
- Clinicians should be encouraged to interpret model outputs, not just act on them. Tree-based models provide that interpretability.

- # Medium Article

- https://medium.com/@agbaoyeadedeji78/alzheimers-disease-analysis-using-tree-based-machine-learning-classification-models-23659bab6172


