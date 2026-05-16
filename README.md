# News-Topic-Classifier-BERT-

Overview
This notebook demonstrates the process of fine-tuning a BERT (Bidirectional Encoder Representations from Transformers) model for news topic classification. Specifically, it uses the AG News dataset to categorize news headlines into one of four classes: World, Sports, Business, or Sci/Tech.

Setup
To run this notebook, you need to install the following Python libraries. You can install them using pip:

pip install datasets transformers[torch] evaluate
Dataset
The project utilizes the AG News dataset, which is a collection of more than 1 million news articles. For demonstration purposes, a small subset of 1000 training samples and 200 test samples is used.

Model
The base model used for fine-tuning is bert-base-uncased from the Hugging Face Transformers library.

Training
The BERT model is fine-tuned for 1 epoch on the small subset of the AG News dataset. Key training parameters include:

Learning Rate: 2e-5
Batch Size: 16 (per device)
Optimizer: AdamW
Evaluation Results
After training, the model was evaluated on the test subset, achieving the following performance metrics:

Evaluation Loss: 0.5443
Evaluation Accuracy: 0.8250
Evaluation F1 Score (weighted): 0.8247
These metrics indicate a reasonable performance for a model trained on a small subset of data.

Usage
To run this notebook, simply execute all cells in sequence. The notebook covers data loading, tokenization, model setup, training, and evaluation.

Next Steps
Full Dataset Training: Train the model on the complete AG News dataset for improved performance.
Hyperparameter Tuning: Experiment with different learning rates, batch sizes, and number of epochs.
Model Deployment: Export the fine-tuned model for deployment in a real-world application.
Error Analysis: Analyze misclassified examples to understand model weaknesses and potential areas for improvement.
