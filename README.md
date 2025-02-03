# Customer_support
•This project classifies customer support tickets using Naive Bayes and Random Forest, with confusion matrix evaluation and manual predictions.

## Project Overview 
This project focuses on classifying customer support tickets into categories like Account Issue, Billing Issue, General Inquiry, Product Inquiry, and Technical Issue. It utilizes machine learning algorithms, specifically Naive Bayes and Random Forest, to predict the category of a given ticket based on its description. The text data is preprocessed using tokenization, stopword removal, and lemmatization, followed by TF-IDF vectorization. The model’s performance is evaluated using confusion matrices and classification reports. The project demonstrates how machine learning can automate ticket categorization, improving efficiency in customer support systems.

## Dataset
This project utilizes the customer support tickets datasets, which includes customer's issues as ticket descriptions and categorized as per the need. This dataset contains 500 rows and 3 columns.

## Execution Plan

### Methodology
The methodology outlines the process of preprocessing customer support tickets, extracting features using TF-IDF, and classifying tickets into categories using Naive Bayes and Random Forest models. It includes data cleaning, stopword removal, and lemmatization to normalize text. The models are trained on labeled data and evaluated using confusion matrices and classification metrics, ensuring accurate ticket categorization. This pipeline ensures scalable and efficient machine learning for automating ticket classification in customer support systems.

1. **Data Collection**: The dataset, "customer_support_tickets.csv," contains customer support ticket descriptions along with their respective categories (e.g., Account Issue, Billing Issue, etc.).

2. **Data Preprocessing**:
   - **Text Cleaning**: Text data is cleaned by converting it to lowercase, removing non-alphabetic characters, and splitting it into words.
   - **Stopword Removal**: Common stopwords (e.g., "the", "is") are removed to reduce noise.
   - **Lemmatization**: Words are reduced to their root form using a WordNet Lemmatizer for better feature representation.

3. **Feature Extraction**:
   - **TF-IDF Vectorization**: Text descriptions are converted into numerical feature vectors using Term Frequency-Inverse Document Frequency (TF-IDF) to capture important words.

4. **Model Selection**:
   - **Naive Bayes (MultinomialNB)**: This algorithm is used to classify tickets based on their feature vectors. It assumes word independence and is effective for text classification tasks.
   - **Random Forest**: A more complex model is used for comparison. It builds multiple decision trees and aggregates their results for improved accuracy.

5. **Model Training**: The dataset is split into training and test sets (80% for training, 20% for testing) using `train_test_split` to evaluate model performance.

6. **Prediction and Evaluation**:
   - The trained models predict the ticket categories on the test set.
   - **Confusion Matrix**: Used to evaluate the models’ classification performance by comparing predicted and actual values.
   - **Classification Report**: Provides detailed metrics like precision, recall, and F1-score for each category.

7. **Results Visualization**:
   - **Heatmap Visualization**: The confusion matrices of both models (Naive Bayes and Random Forest) are visualized using heatmaps for better interpretation of the results.

8. **Prediction Function**: A custom function is created to predict the category of a new ticket description based on preprocessed input.

## Results
The models, Naive Bayes and Random Forest, were evaluated on the test set using confusion matrices and classification metrics.

- **Naive Bayes**:
  - The confusion matrix showed a good classification of categories, though some misclassifications occurred between similar categories (e.g., Billing and Account Issues).
  - The classification report highlighted solid precision, recall, and F1-score values for each category, demonstrating the model's capability to handle text classification tasks effectively.

- **Random Forest**:
  - The confusion matrix for Random Forest displayed a higher accuracy in classifying categories compared to Naive Bayes, particularly for technical and product-related issues.
  - The classification report showed improved performance, with higher F1-scores across most categories, making it a more robust choice for ticket classification.

Both models performed well, with Random Forest slightly outperforming Naive Bayes in accuracy and category differentiation.

**Confusion Matrix Heatmaps**:
- Visualizing the confusion matrices for both models using heatmaps helped identify areas of misclassification, enabling further improvements for better performance in real-world applications.
