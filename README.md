# Content Tagging with NLP using deep learning

## Overview

Content tagging is a way of organizing and categorizing information on websites, social media, forums, and question-and-answer platforms. It involves assigning labels or tags to pieces of content, such as posts, articles, or questions, to make them easily searchable and accessible.
steps to develop a deep learning model for this task and also the tools I've used include:

- Preparing data:
  1- Used NLTK for Tokenization
  2- Removed punctuation and digits
  3- Converted to lowercase

- Data Preprocessing:
  1. Converted the text data into a numerical format that can be fed into a deep learning model.
  2. Used Dataset and Dataloader in 'torch.utils.data' to prepare datasets and handle batches of training and validation data.
  3. Tokenized input text using the BERT tokenizer and convert it into a format suitable for BERT input.
 
- Designing and Training the model:
  1. Created the customized model BertMultilabel, Followed by a Droput and Linear Layer on top of Bert to get the final output for the model.
  2. Used BCEWithLogitsLoss Function that combines a Sigmoid layer and the Binary Cross Entropy Loss in a single class. It's computationally more stable than applying a sigmoid activation function separately followed by a BCE Loss.  

- fine-tuning model:
    defined a training function that trains the model on the training dataset, specified number of times (EPOCH).
- Validating the Model:
    Accuracy Score, F1 Micro, and F1 Macro are used to get a measure of model performance

