# **User Journey Analysis**

This project leverages user behavioural data to predict whether the last checkpoint of a user's journey is the **Checkout** page. The analysis uses machine learning techniques, primarily logistic regression, to understand patterns in user behavior and improve user experience.

---

## **Project Structure**

### **1. Data**
The dataset obtained from https://learn.365datascience.com/projects/user-journey-analysis-in-python/ contains information about user journeys on a website. Key columns include:
- **`journey_length`**: Total number of pages visited in a user's journey.
- **`Homepage`**: Count or presence of visits to the Homepage.
- **`Pricing`**: Count or presence of visits to the Pricing page.
- **`Checkout`**: Count or presence of visits to the Checkout page.
- **`last_checkpoint`**: The final page visited in the journey.

### **2. Model**
The project uses a **Logistic Regression** model to predict the target:
- **Target (`y`)**:
  - A binary variable where:
    - `1` = Last checkpoint is the **Checkout** page.
    - `0` = Last checkpoint is any other page.
- **Features (`X`)**:
  - `journey_length`
  - `Homepage`
  - `Pricing`
  - `Checkout`

### **3. Metrics**
The model's performance is evaluated using:
- **Classification Report**:
  - Precision, Recall, F1-Score.
- **ROC Curve**:
  - Measures the model's ability to distinguish between classes.
  - Area Under the Curve (AUC = 0.91) indicates excellent performance.
- **Precision-Recall Curve**:
  - Evaluates the trade-off between precision and recall, especially useful for imbalanced datasets.

---

## **Project Workflow**

1. **Data Preparation**:
   - The dataset is preprocessed to include relevant features and convert the target variable into a binary format.

2. **Model Training**:
   - Data is split into training (70%) and testing (30%) sets.
   - The Logistic Regression model is trained on the training data.

3. **Model Evaluation**:
   - The model is tested on unseen data (test set) and evaluated using metrics and visualisations:
     - **ROC Curve**: Evaluates overall classification performance.
     - **Precision-Recall Curve**: Highlights the balance between false positives and false negatives.

4. **Insights**:
   - **Features**: The model identifies key factors influencing whether a user's last checkpoint is the **Checkout** page.
   - **Optimisation Opportunities**: The results can guide UX improvements, reduce drop-offs, and optimise navigation flows.

---

