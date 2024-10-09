# Spaceship Titanic Prediction Project

**Duration:** August 2024 – October 2024  
**Objective:** Achieve over 80% accuracy in predicting passenger survival on the fictional Spaceship Titanic.

## Project Overview:

This project focuses on solving the [Spaceship Titanic competition](https://www.kaggle.com/competitions/spaceship-titanic) problem from Kaggle, where the goal is to predict whether a passenger survived the disaster based on various features such as age, home planet, fare, and spending behavior on the ship.

By employing machine learning models, I worked through key tasks like **data preprocessing**, **feature engineering**, and **model tuning** to maximize the predictive power of the models.

## Key Achievements:

- **Achieved 80% accuracy** on the test dataset by implementing a combination of feature engineering and advanced models.
- Applied **Random Forests** and **XGBoost** as the core models after testing various machine learning algorithms.
- Implemented **grid search** and **cross-validation** to optimize hyperparameters, improving model generalization and preventing overfitting.
- Utilized key features like *'CryoSleep'*, *'TotalSpent'*, and *'CabinDeck_Side'* to reveal hidden relationships that significantly impacted prediction accuracy.

## Technical Details:

### 1. Data Preprocessing:
- Handled missing values, especially in the **CryoSleep** and **Fare** features.
- Created new features like **log transformations** for spending and fare, polynomial features, and feature interactions.
- **One-hot encoded** categorical variables like *CabinDeck_Side*, which captured adjacency and positional data on the ship.

### 2. Feature Engineering:
- **CryoSleep Logic:** Passengers marked as in **CryoSleep** had no spending, a key rule that led to the creation of interaction features such as **CryoSleep_Age_Interaction** and **CryoSleep_VIP**.
- **Group Spending Features:** Aggregated spending values for passengers traveling in the same group, creating variables like **GroupTotalSpent** and **GroupSize**.
- **Deck-Level Interactions:** Calculated the average **CryoSleep rate** for each cabin side and deck, along with other deck-related interactions.

### 3. Modeling:
- Tested multiple models, including **Logistic Regression**, **Random Forest**, **XGBoost**, and **LightGBM**.
- Final models—**Random Forests** and **XGBoost**—were chosen for their superior accuracy and ability to handle complex feature interactions.
- **Grid Search** was conducted for hyperparameter tuning, refining max depth, learning rate, and the number of estimators.

### 4. Validation:
- **Cross-validation methods** ensured the model’s generalizability across different subsets of the data.
- Validation accuracy reached **79.9%**, and the final model achieved **80% accuracy** on the test set.

### 5. Insights:
- The **feature importance analysis** revealed that *CryoSleep*, *Age*, and *CabinDeck_Side* were among the most impactful factors for predicting survival.
- The creation of **interaction terms** and **spending-based features** added significant value to the model’s performance.

## Future Directions:

- **Model Interpretability:** Future work will focus on enhancing interpretability by using models like **SHAP** (SHapley Additive exPlanations) to explain feature importance and passenger predictions.
- **Further Feature Engineering:** Explore more complex feature interactions and dimensionality reduction techniques such as **PCA** (Principal Component Analysis) to simplify the model without sacrificing accuracy.
- **Automating Pipelines:** I plan to integrate the model into a **CI/CD pipeline** using **TFX** (TensorFlow Extended) for seamless deployment.

## Tools & Technologies Used:

- **Python** for data analysis and modeling
- **Pandas**, **NumPy** for data manipulation
- **Scikit-learn**, **XGBoost**, **LightGBM** for machine learning
- **Matplotlib**, **Seaborn** for data visualization
- **Jupyter Notebook** for iterative development and exploration
- **Grid Search** and **Cross-Validation** for hyperparameter tuning
