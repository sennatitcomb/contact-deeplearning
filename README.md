# Contact Database Format
Transformer model API to process and validate CSV data
* This code utilizes a mix of good and bad data. Some of which was sampled and cleaned from Kaggle (https://www.kaggle.com/datasets/ravindrasinghrana/employeedataset/data)
* The performance of predictions will change depending on the quality and amount of data that the model uses to train.

Key Steps:

1. Model and Tokenizer Initialization:
The script initializes a pre-trained BERT-based model for sequence classification and its corresponding tokenizer from the Hugging Face Transformers library.

2. CSV File Processing:
The script reads a CSV file containing data with columns such as "First Name," "Last Name," "Email," "Phone," and "Title."

3. Tokenization and Prediction:
Each column of the data is tokenized separately using the loaded tokenizer. The resulting tensors are then used as input for the model to predict whether each row conforms to the expected "good" or "bad" data format.

4. Output Display:
The script displays the processed data along with the predicted labels for each row, indicating whether the model categorizes the data as "good" (label 0) or "bad" (label 1).

5. Input Text Parsing and Classification: The script now accepts input text containing information such as "First Name," "Last Name," "Title," "Email," and "Phone." It dynamically adapts to variations in input formatting, including cases where only the first and last names are space-separated while other columns are tab-separated. The input text is tokenized and fed into the model for predictions.

6. Threshold-based Classification for Input Text: Similar to the CSV data processing, the script employs a threshold-based classification approach for input text. It checks the probability for the negative class against a user-defined threshold. If the probability exceeds the threshold, the input is classified as "Negative"; otherwise, it is labeled as "Positive."

7. CSV Output Creation: After parsing and classifying the input text, the script constructs a CSV file with columns such as "First Name," "Last Name," "Title," "Email," "Phone," and "Predicted Label." The CSV file captures the model's predictions and serves as a structured representation of the processed input text.

8. Adjustable Threshold: Users can customize the threshold value to influence the model's sensitivity to deviations in input formatting. This flexibility allows users to strike a balance between precision and recall when classifying input text.

9. Enhanced Output Display: The script displays detailed information, including raw logits, class probabilities, and the predicted category (Positive or Negative), providing users with insights into the model's decision-making process.
