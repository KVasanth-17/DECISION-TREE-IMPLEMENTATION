# DECISION-TREE-IMPLEMENTATION

*COMPANY*: CODTECH IT SOLUTIONS

*NAME*: VASANTH KANDIBANDA

*INTERN ID*: CT08DZ1238

*DOMAIN*: MACHINE LEARNING

*DURATION*: 8 WEEEKS

*MENTOR*: NEELA SANTOSH

*DESCRIPTION OF THE TASK*: 

# 📊 Decision Tree Classification on Breast Cancer Dataset

This project demonstrates how a **Decision Tree Classifier** can be applied to the **Breast Cancer dataset** from `scikit-learn` to predict whether a breast tumor is **benign (non-cancerous)** or **malignant (cancerous)**. Decision trees are a type of supervised learning algorithm that are highly interpretable, meaning you can literally follow the “if-else” logic to see how the model arrives at its predictions. This makes them particularly useful in healthcare applications where **explainability is crucial**.

The main idea is simple: take real medical data, train a model to learn patterns from past tumor samples, and then use it to classify new unseen samples. Along the way, we also visualize the decision tree so that the decision-making process becomes transparent and easy to understand.

---

## 🧾 What’s Inside the Notebook?

The notebook walks you through the entire machine learning workflow:

### 1. Loading the Dataset
- The Breast Cancer dataset contains **569 samples** and **30 numerical features** describing tumor characteristics, such as radius, texture, perimeter, smoothness, and compactness.  
- Each sample is labeled as either:
  - **Malignant** → Cancerous tumor  
  - **Benign** → Non-cancerous tumor  

### 2. Splitting the Data
- Data is split into **80% training** and **20% testing**.  
- This ensures the model learns patterns from the training set and is evaluated on unseen data.  
- Stratification keeps both classes proportionally represented in training and testing sets.  

### 3. Building the Decision Tree
- A Decision Tree Classifier is used because it is **interpretable** and can handle numerical features without scaling.  
- Key parameters include:
  - `criterion="entropy"` to use information gain for splits  
  - `max_depth=4` to prevent overfitting  

### 4. Training the Model
- The tree learns splitting rules at each node, recursively dividing the data to separate benign from malignant tumors.  

### 5. Making Predictions & Evaluation
- Predictions are made on the test set.  
- The model is evaluated using:
  - **Accuracy** – overall correctness of predictions  
  - **Precision** – proportion of predicted positives that are actually positive  
  - **Recall** – proportion of actual positives correctly predicted  
  - **F1-Score** – balance between precision and recall  
  - **Confusion Matrix** – shows true positives, true negatives, false positives, and false negatives  
- High recall for malignant tumors is critical in medical applications to minimize false negatives.  

### 6. Visualizing the Tree
- Using `plot_tree`, the trained model is visualized to show:
  - Features used for splits  
  - Thresholds applied at each node  
  - Predicted class distributions at leaves  
- This provides a clear view of the model’s **decision-making process**.  

### 7. Predicting New Samples
- The model is demonstrated on a single test sample.  
- Predictions are compared with actual labels to show how the model can classify new patient data.

---

## 📈 Results
- **High accuracy**, typically above 90%, on the test dataset.  
- Reliable detection of **malignant tumors**, which is critical in healthcare.  
- Decision tree visualization provides clear insight into **how predictions are made**.  

---

## 🔑 Key Takeaways
- Decision Trees are **interpretable, fast, and effective** for classification tasks.  
- Limiting tree depth prevents overfitting while maintaining performance.  
- Visualization helps explain **how the model makes decisions**.  
- Understanding evaluation metrics ensures the model meets practical requirements.  

---

## 🚀 Extensions
- Plot **feature importance** to identify which tumor characteristics most influence predictions.  
- Compare with ensemble methods like **Random Forests** or **Gradient Boosting** for improved accuracy.  
- Implement **cross-validation** to ensure robust performance.  
- Deploy the model using **Flask** or **FastAPI** for real-world usage.  

---

## 🎯 Conclusion
This notebook provides a **hands-on demonstration of interpretable machine learning** applied to a real medical dataset. It shows how Decision Trees can balance **accuracy and transparency**, making them a valuable tool for students, practitioners, and researchers alike.  

By visualizing the tree and evaluating predictions, the project demonstrates the practical use of machine learning in healthcare while keeping the model **explainable and trustworthy**.


*OUTPUT*: 

Feature names: ['mean radius' 'mean texture' 'mean perimeter' 'mean area'
 'mean smoothness'] ...
 
Target names: ['malignant' 'benign']

Accuracy: 0.8947368421052632

<img width="501" height="393" alt="Image" src="https://github.com/user-attachments/assets/48c8b47e-9ae7-4970-adaf-fb03b2deae2b" />


<img width="640" height="812" alt="Image" src="https://github.com/user-attachments/assets/d42b8d4b-568c-41c4-aa60-78a2180d4966" />


New Sample Prediction: malignant

Actual Label: malignant

### 📑 Classification Report

```text
               precision    recall  f1-score   support

   malignant       0.80      0.95      0.87        42
      benign       0.97      0.86      0.91        72

    accuracy                           0.89       114
   macro avg       0.88      0.91      0.89       114
weighted avg       0.91      0.89      0.90       114




