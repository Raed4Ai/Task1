Toxic Comment Classification project
# This is the first version of this project, that I will modify and it.


A multi-label text classification project for detecting toxic comments. The model analyzes text and predicts whether it contains one or more of the following categories:

- `toxic`
- `severe_toxic`
- `obscene`
- `threat`
- `insult`
- `identity_hate`

## Models Used

- **RNN** (Simple Recurrent Neural Network)
- **LSTM** (Long Short-Term Memory)

## Workflow
1. **Text Preprocessing:** Cleaning the text, removing stopwords, and lemmatizing words using NLTK.
2. **Text Vectorization:** Converting text into numerical representation using TensorFlow's `TextVectorization`.
3. **Data Splitting:** Using `IterativeStratification` to ensure a balanced distribution of the multiple labels across training and test sets.
4. **Model Building:** Training RNN and LSTM models using Embedding, Dropout, and GlobalMaxPooling1D layers.
5. **Evaluation:** Measuring performance using F1 Score, Precision-Recall Curve, and Classification Report.

#Results 
Both models achieved good and comparable performance on the validation set (Weighted F1 ≈ 0.74), 
particularly for the major categories (toxic, obscene, insult). However, performance was poor on the official Kaggle test set 
(Weighted F1 ≈ 0.57–0.62) due to the challenging nature of the data, with both models showing weaker results 
on the minority categories (threat, severe_toxic) caused by severe class imbalance.

## Requirements
See [requirements.txt](./requirements.txt) for all libraries needed to run this project.

## License
This project is licensed under the [Apache License 2.0](./LICENSE).
