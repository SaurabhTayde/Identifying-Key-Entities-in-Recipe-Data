# Identifying Key Entities in Recipe Data

```
###################################################################################
###
###  Case Study Name        :  Identifying Key Entities in Recipe Data
###
###  Case Study Goal        :  To automatically convert unstructured recipe text
###                           into structured, actionable data (quantity, unit,
###                           ingredient) to power new digital features and
###                           business analytics.
###
###  Author                 :  Saurabh Tayde
###
###  Email                  :  saurabhtayde2810@gmail.com
###
###  Date                   :  9th July 2025
###
###################################################################################
```

## Project Overview

This project addresses the critical business challenge of unstructured recipe data. Raw ingredient text, such as `"2 1/2 cups of all-purpose flour"`, contains valuable information that is inaccessible to automated systems. This initiative successfully developed an intelligent model to parse this text and extract its core entities: **`Quantity`**, **`Unit`**, and **`Ingredient`**.

The outcome is a production-ready AI asset that transforms raw text into structured, actionable data, enabling a new suite of digital features and analytical capabilities.

## Our Approach: A Data-Driven Methodology

A systematic, five-step methodology was employed to ensure a robust and reliable solution:

1.  **Data Analysis and Preparation:** We began by performing an Exploratory Data Analysis (EDA), which revealed a critical insight: the data was heavily imbalanced, with nearly 75% of all tokens labeled as `Ingredient`. This discovery was crucial in shaping our modeling strategy.

2.  **Advanced Feature Engineering:** To enable the model to understand language context, we engineered a rich set of features for each word. This included linguistic cues (e.g., part-of-speech), contextual clues (e.g., surrounding words), and custom patterns (e.g., identifying fractions and digits).

3.  **Conditional Random Field (CRF) Model Selection:** We chose a CRF model, a state-of-the-art technique for sequence labeling. Its strength lies in its ability to consider the entire sequence of words, allowing it to learn grammatical and structural patterns like `Quantity` is often followed by `Unit`.

4.  **Balanced Training Strategy:** To overcome the data imbalance identified in our analysis, we implemented a class weighting strategy. This technique instructed the model to pay significantly more attention to the rarer `Quantity` and `Unit` labels, ensuring it learned to identify all three categories effectively.

5.  **Rigorous Evaluation and Error Analysis:** The model was tested against a reserved, unseen validation dataset. We went beyond simple accuracy metrics, conducting a deep-dive error analysis to understand precisely where and why the model made mistakes.

## Performance & Results

The final model demonstrates exceptional performance, proving its readiness for real-world application.

*   **Overall Accuracy on Unseen Data:** **98.23%**
*   **Model Generalization:** A minimal performance drop of less than 1% from the training set, indicating a robust and well-generalized model.

#### **Performance by Category (F1-Score):**
*   **Quantity:** `0.9890` (Near-perfect)
*   **Ingredient:** `0.9887` (Near-perfect)
*   **Unit:** `0.9356` (Strong)

## Key Insights & Business Outcomes

This project delivered more than just a model; it produced actionable insights and tangible business value.

#### **Key Insights:**
*   **The Model is Predictable:** The model's primary weakness is a specific, understandable challenge: distinguishing between ambiguous `Unit` and `Ingredient` tokens (e.g., "cloves"). This predictability makes the model reliable.
*   **Context is King:** The model's success proves that context-aware AI is vastly superior to simple keyword matching for understanding language.
*   **Data Preparation Drives Success:** The careful analysis of data imbalance and the subsequent weighting strategy were the most critical factors in achieving high performance across all categories.

#### **Business Outcomes:**
*   **A Deployed AI Asset:** A saved, trained model (`crf_model.pkl`) that is a reusable and scalable software component.
*   **Activation of New Capabilities:** The structured data output enables immediate implementation of high-value features like automated nutritional analysis, e-commerce shopping lists, and advanced recipe search filters.
*   **A Proven Blueprint for Future AI Projects:** This project establishes a successful methodology that can be replicated to accelerate future AI development.



For any questions or collaboration inquiries, please contact Saurabh Tayde at `saurabhtayde2810@gmail.com`.
