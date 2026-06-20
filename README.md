Customer Support Ticket Classification & Prioritization

Future Interns – Machine Learning Task 2

Project Overview

This project focuses on automatically classifying and prioritizing customer support tickets using Machine Learning and NLP techniques. Support teams receive hundreds of tickets daily — manually sorting them is slow and inefficient.

The goal of this project was to build a system that reads ticket text, predicts the ticket category, and assigns a priority level so that urgent issues get handled first.

Dataset

This project uses the Customer Support Ticket Dataset, which contains real customer support records including ticket descriptions, categories, and priority levels.

Dataset Source: https://www.kaggle.com/datasets/suraj520/customer-support-ticket-dataset

Project Workflow

1. Data Loading & Exploration

Loaded and inspected the dataset (8,469 tickets)
Checked for missing values
Analyzed distribution of ticket types and priorities

2. Text Cleaning

Applied NLP preprocessing steps:
Converted text to lowercase
Removed punctuation and special characters
Removed stopwords (common words like "the", "is", "a")
Applied stemming to reduce words to their root form

3. Feature Extraction

Used TF-IDF Vectorizer (top 5000 features, unigrams + bigrams)
Converted cleaned ticket text into numerical features that ML models can understand

4. Model Building

Two separate classification tasks were trained:
Ticket Type Classification — predicts the category of a ticket
Ticket Priority Prediction — predicts the urgency level

Three models were tested for each task:
Naive Bayes
Logistic Regression
Random Forest Classifier

5. Model Evaluation
Models were evaluated using:
Accuracy
Precision, Recall, F1-Score
Confusion Matrix
Class-wise performance analysis

Ticket Types
Technical issue
Billing inquiry
Cancellation request
Product inquiry
Refund request

Priority Levels
Critical
High
Medium
Low

Results

| Model               | Ticket Type Accuracy | Priority Accuracy |
|---------------------|---------------------|--------------------|
| Naive Bayes         | ~% 19.01            | ~% 24.91           |
| Logistic Regression | ~% 19.42            | ~% 25.03           |
| Random Forest       | ~% 19.60            | ~% 25.05           |

Live Prediction

The notebook includes a predict_ticket() function that takes any ticket description and instantly predicts its type and priority with confidence percentage.

Example:

Input   : "I was charged twice for my subscription and need a refund!"
Type    : Billing inquiry   (91.3% confident)
Priority: High             (78.5% confident)

Business Insights
This system can help businesses:
Automatically route tickets to the right support team
Instantly flag Critical and High priority tickets for faster response
Reduce time agents spend manually reading and sorting tickets
Handle large volumes of tickets without adding more staff
Improve overall customer satisfaction through faster resolution

Limitations
Model accuracy depends on the quality and length of ticket descriptions
Very short or vague tickets may not classify well
The model should be retrained periodically as new ticket types appear

Conclusion
This project shows how NLP and Machine Learning can be applied to a real business problem. By automating ticket classification and prioritization, support teams can focus on solving issues rather than sorting them.

Author — by Devaki
