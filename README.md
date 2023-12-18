# Contact Database Format
Transformer model API to process and validate CSV data
* This code utilizes a mix of good and bad data. Some of which was sampled and cleaned from Kaggle (https://www.kaggle.com/datasets/ravindrasinghrana/employeedataset/data)
* The performance of predictions will change depending on the quality and amount of data that the model uses to train.

Key Steps:

Model and Tokenizer Initialization:
The script initializes a pre-trained BERT-based model for sequence classification and its corresponding tokenizer from the Hugging Face Transformers library.

CSV File Processing:
The script reads a CSV file containing data with columns such as "First Name," "Last Name," "Email," "Phone," and "Title."

Tokenization and Prediction:
Each column of the data is tokenized separately using the loaded tokenizer. The resulting tensors are then used as input for the model to predict whether each row conforms to the expected "good" or "bad" data format.

Output Display:
The script displays the processed data along with the predicted labels for each row, indicating whether the model categorizes the data as "good" (label 0) or "bad" (label 1).
