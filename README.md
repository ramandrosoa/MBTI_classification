# MBTI Types Analysis and Prediction on Textual Data

This [notebook](MBTI_NLP.ipynb) contains a comprehensive analysis and classification of MBTI (Myers-Briggs Type Indicator) types based on textual data. The project focuses on extracting meaningful features from text and employing various machine learning algorithms to classify the data accurately.

## Features Engineering

To understand and analyze the textual data effectively, the following features were engineered:

1. **Post Length**: The word count of each post (excluding links) was calculated to capture the conciseness of writing styles.

2. **Readability (Gunning Fox Index)**: This index was used to gauge the complexity of writing by analyzing sentence length and word difficulty.

3. **Named Entity Recognition (NER)**: NER was applied to capture differences in focus across various personality types, helping to identify key themes and topics.

4. **Sentiment Analysis (Polarity Scores)**: The emotional tone of posts was analyzed to determine the sentiment expressed, providing insight into how different MBTI types may convey emotions.

5. **Vectorization**: Text was converted into numerical form using methods such as TF-IDF and word embeddings. This representation allows for the assessment of word importance and meaning in machine learning models.

## Data Resampling

Given the imbalanced nature of the dataset, resampling techniques were applied to the training set to ensure balanced representation of MBTI types:

- **Undersampling**: For types that were overrepresented in the dataset compared to their actual proportions, undersampling was utilized to reduce their representation.

- **Oversampling**: For types that were underrepresented, oversampling was applied to increase their representation and balance the dataset.

## Classification

The MBTI types were broken down into four binary classifications:

- **I vs. E** (Introversion vs. Extraversion)
- **N vs. S** (Intuition vs. Sensing)
- **T vs. F** (Thinking vs. Feeling)
- **J vs. P** (Judging vs. Perceiving)

### Model Training and Evaluation

The following classifiers were used for training:

- **Logistic Regression**
- **KNeighbors Classifier**
- **RandomForest Classifier**

Grid Search was employed to identify the best model and hyperparameters for each classifier, optimizing for the highest cross-validation score. The performance of the models was evaluated using:

- **Confusion Matrix**
- **Precision and Recall**
- **F1 Score**

## Predictions

Finally, predictions were made on textual data sourced from social media and discussion platforms, providing practical insights into the application of the model.

## References

[Distribution of Personality Types in Percentages](https://personalitymax.com/personality-types/population-gender/)
[Predicting Myers-Briggs Type Indicator with Text Classification](https://web.stanford.edu/class/archive/cs/cs224n/cs224n.1184/reports/6839354.pdf)
