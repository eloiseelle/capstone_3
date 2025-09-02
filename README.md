
![netflix banner](https://github.com/user-attachments/assets/63636371-354c-4433-af73-a2757e7f00f0)


# Netflix Customer Churn: Identifying the Behavioral Drivers of User Retention 

## 1. Project overview

Netflix faces persistent customer churn, which erodes recurring revenue and limits upselling opportunities. In a highly competitive streaming market with rising acquisition costs and subscription fatigue, retaining existing subscribers is more profitable than constantly acquiring new ones.

This project analyzes Netflix’s 2025 User Behavior Dataset to identify the behavioral drivers of churn, build a prediction model, and deliver actionable recommendations to reduce cancellations.


## 2. Objectives

* Develop a churn prediction model despite significant class imbalance (85% active, 15% churn).
* Identify behavioral drivers of retention versus departure.
* Provide concrete recommendations to improve retention ROI.

## 3. Key findings

* **Churn distribution**: 85% active, 15% churned.
* **Early tenure is risky**: most churn happens within the first 90 days.
* **Engagement drives loyalty**: high watch time and completion rates strongly reduce churn risk.
* **Discovery matters**: active searchers and recommendation clickers are more likely to stay.
* **Satisfaction predicts churn**: low ratings and negative reviews often precede cancellations.
* **Static attributes are weak predictors**: demographics and plan tiers have little impact compared to behavior.

## 4. Modeling results

We compared four models using PR AUC as the primary metric (due to class imbalance):

| Model                          | ROC AUC   | PR AUC    | Recall    | Precision | Notes                                              |
| ------------------------------ | --------- | --------- | --------- | --------- | -------------------------------------------------- |
| Dummy (majority baseline)      | 0.500     | 0.148     | 0.000     | 0.000     | Always predicts majority class                     |
| Logistic Regression (balanced) | 0.440     | 0.133     | 0.405     | 0.124     | High recall, very low precision                    |
| Random Forest (balanced)       | 0.492     | 0.140     | 0.000     | 0.000     | Collapsed to majority class                        |
| XGBoost (final)                | 0.510     | 0.153     | 0.125     | 0.148     | Best performance. Small but consistent improvement |

**Interpretation:** Even though performance gains were modest, XGBoost demonstrated the ability to detect weak behavioral patterns where other models failed.

## 5. Recommendations

* **Strengthen onboarding**: Offer personalized starter packs, reminders to finish shows, and highlight recommendation features during the first 90 days, when churn risk is highest.
* **Monitor satisfaction**: Identify users who give low ratings or negative reviews and reach out with personalized content or offers.
* **Focus on high-value customers**: Estimate Customer Lifetime Value (CLV = monthly spend × tenure) and and direct retention resources toward high-value subscribers most at risk.

## 6. Future work

* Build richer features (recency, engagement decay and interactions).
* Apply survival analysis to study how churn risk changes over time.
* Validate interventions through controlled A/B testing to measure impact on churn and revenue.

---

## 📧 Contact

**Author:** Éloïse Bouton

LinkedIn: https://www.linkedin.com/in/eloisebouton/

This project is part of the **Springboard Data Science Career Track – Capstone Project 3**.

