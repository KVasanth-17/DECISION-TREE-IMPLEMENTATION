# DECISION-TREE-IMPLEMENTATION

*COMPANY*: CODTECH IT SOLUTIONS

*NAME*: VASANTH KANDIBANDA

*INTERN ID*: CT08DZ1238

*DOMAIN*: MACHINE LEARNING

*DURATION*: 8 WEEEKS

*MENTOR*: NEELA SANTOSH

*DESCRIPTION OF THE TASK*: 

📊 Decision Tree Classification on Breast Cancer Dataset

This project demonstrates how a Decision Tree Classifier can be applied to the Breast Cancer dataset from scikit-learn to predict whether a breast tumor is benign (non-cancerous) or malignant (cancerous). Decision trees are a type of supervised learning algorithm that are highly interpretable, meaning you can literally follow the “if-else” logic to see how the model arrives at its predictions. This makes them particularly useful in healthcare applications where explainability is crucial.

The main idea is simple: take real medical data, train a model to learn patterns from past tumor samples, and then use it to classify new unseen samples. Along the way, we also visualize the decision tree so that the decision-making process becomes transparent and easy to understand.

The notebook walks you through the entire machine learning workflow:

Loading the Dataset
The Breast Cancer dataset contains 569 samples and 30 numerical features describing tumor characteristics, such as radius, texture, perimeter, smoothness, and compactness. Each sample is labeled as either malignant (cancerous) or benign (non-cancerous).

Splitting the Data
Data is split into 80% training and 20% testing. This ensures that the model can learn patterns from the training set and then be evaluated on unseen data. Stratification keeps both classes proportionally represented.

Building the Decision Tree
A Decision Tree Classifier is used because it is interpretable and can handle numerical features without scaling. Key parameters include criterion="entropy" for information gain and max_depth=4 to prevent overfitting.

Training the Model
The model learns splitting rules at each node, recursively dividing the data to separate benign and malignant tumors.

Making Predictions & Evaluation
Predictions are made on the test set, and the model is evaluated using accuracy, precision, recall, F1-score, and a confusion matrix. High recall for malignant tumors is critical in medical applications to minimize false negatives.

Visualizing the Tree
Using plot_tree, the trained model is visualized to show which features are used for splits, the thresholds applied, and the predicted class distributions. This makes the model’s decision-making process easy to understand.

Predicting New Samples
The model is demonstrated on a single test sample, showing how it can classify new patient data and compare predictions with actual labels.

Overall, the decision tree achieves high accuracy, reliably detects malignant tumors, and provides a clear, interpretable view of the classification process. This makes it an excellent example of applying interpretable machine learning to real-world medical data, balancing accuracy and transparency.

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




