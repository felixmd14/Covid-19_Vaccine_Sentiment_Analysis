# COVID-19 VACCINE SENTIMENT ANALYSIS

## Introduction

This project's primary goal is to develop a Machine Learning model for analyzing sentiments expressed in Twitter posts related to COVID-19 vaccinations. The model aims to classify these tweets as either positive, negative, or neutral. The insights gained from this analysis can be instrumental for governments and public health entities to monitor public sentiment regarding COVID-19 vaccinations, which, in turn, can assist in refining public health policies, communication strategies, and vaccination programs on a global scale.

## Natural Language Processing

In this project, we work with text data, which initially exists in a non-numerical format. Before we can utilize it in a Machine Learning model, the text data must undergo preprocessing to convert it into a suitable format for analysis. This process is made possible through Natural Language Processing (NLP), which involves the computer's ability to understand and interpret human language as it is spoken or written.

## Sentiment Analysis

Sentiment analysis is the process of evaluating digital text to determine whether the emotional tone of the message is positive, negative, or neutral. In today's data-rich world, companies have access to vast amounts of textual data, including emails, customer support chat transcripts, social media comments, and reviews. Sentiment analysis tools can automatically assess the author's attitude toward a particular subject. The insights derived from sentiment analysis are widely used by companies to enhance customer service and bolster their brand reputation.

## Leveraging Hugging Face for Sentiment Analysis

Hugging Face is an open-source platform that provides access to machine learning technologies. Users can either directly employ pre-built models or fine-tune them on their own datasets. Additionally, they can host their trained models on the platform for future use on various devices and applications. To get started, please visit the Hugging Face website and sign in to access its full suite of features.

To facilitate sentiment analysis, we employ deep learning-based models from Hugging Face. These models are computationally intensive and typically require substantial GPU power for training. You can consider using Google Colab (https://research.google.com/colab) or your preferred GPU cloud provider, or a local machine equipped with an NVIDIA GPU to train these models effectively.

## Data Description

The data for this project is sourced from tweets collected and categorized through Crowdbreaks.org. These tweets have been classified into three categories: pro-vaccine (1), neutral (0), and anti-vaccine (-1). Notably, the tweets have had usernames and web addresses removed for privacy and data quality reasons.

The primary objective of this challenge is to develop a machine learning model capable of determining whether a given Twitter post related to vaccinations carries a positive, neutral, or negative sentiment.

### Data Understanding

To achieve this objective, it's essential to thoroughly understand the dataset. The data includes the following files:

- `variable_definitions.csv`: This file provides descriptions of the various variables in the dataset.
- `sampleSubmission.csv`: It illustrates the structure of the submission file.
- `train.csv`: This file contains the key data and variables required for training the final model. It can be divided into training and testing sets for local testing.
- `CaptureSite_category.csv`: This file contains information about capture sites and their categories.

Given the nature of this sentiment analysis challenge, the textual variables are of primary importance.

For this challenge, the following four variables are relevant:

- `tweet_id`: A unique identifier for each tweet.
- `safe_tweet`: The text content of the tweet, with sensitive information such as usernames and URLs removed.
- `label`: The sentiment label of the tweet (-1 for negative, 0 for neutral, 1 for positive).
- `agreement`: Since the tweets were labeled by three different reviewers, the agreement column indicates the percentage of agreement among these reviewers. This column can be used for training, but agreement data will not be available for the test set.

### Available Files

The following files are available for download:

- `Train.csv`: This file contains labeled tweets, which can be used for training your sentiment analysis model.
- `Test.csv`: This dataset contains tweets that you must classify using your trained model.
- `SampleSubmission.csv`: This file serves as an example of what your submission file should look like. The order of the rows is not crucial, but the ID names must be correct. The values in the 'label' column should range between -1 and 1.

- `NLP_Primer_twitter_challenge.ipynb`: This is a starter notebook to assist you in making your initial submission to the challenge.

## Setup

To run the evaluation locally, install the required packages. Here are the steps:

1. Ensure you have Python3 installed on your system.
2. Clone this repository and navigate to its root directory (where the repository is located).

### For Windows:

```bash
python -m venv venv
venv\Scripts\activate
python -m pip install -q --upgrade pip
python -m pip install -qr requirements.txt
```

### For Linux & MacOs:

```bash
python3 -m venv venv
source venv/bin/activate
python -m pip install -q --upgrade pip
python -m pip install -qr requirements.txt
```

The long command-lines provided above have the same structure; they chain multiple commands using the semicolon (;). Alternatively, you can manually execute them one after another.

The steps are as follows:

1. Create a Python virtual environment to isolate the required libraries for this project, preventing conflicts.
2. Activate the Python virtual environment to ensure that the Python kernel and libraries are isolated.
3. Upgrade Pip to the latest version to ensure proper package management.
4. Install the required libraries and packages listed in the 'requirements.txt' file to enable their usage in Python scripts and notebooks. Note: MacOs users should install Xcode if they encounter any issues.

## Bert Model

The project leverages Bidirectional Encoder Representations from Transformers (BERT), which is a state-of-the-art model based on transformers developed by Google. BERT can be pre-trained and subsequently fine-tuned for specific tasks.

BERT was pre-trained on the BooksCorpus dataset and English Wikipedia, achieving state-of-the-art results in eleven natural language processing tasks. It was trained on two tasks simultaneously:

1. Masked language modeling (MLM) - Predicting the masked word for 15% of the tokens.
2. Next Sentence Prediction (NSP) - Predicting whether sentence B follows sentence A.

BERT's design enables it to pre-train deep bidirectional representations from unlabeled text, considering both left and right context in all layers. Consequently, a pre-trained BERT model can be fine-tuned with just one additional output layer to create state-of-the-art models for various tasks, such as question answering and language inference, without substantial task-specific architecture modifications.

BERT comes in several variants, including "bert-base-uncased" and "bert-base-cased," which differ in their tokenization strategies. Additionally, there are larger versions of BERT with more parameters for improved performance.

## Feedback and Support

If you have any questions or need assistance, please feel free to create an issue in the GitHub repository. You can also contact the author, Felix Kiprono Bett, via email at felixmd14@gmail.com or connect with him on LinkedIn: [Felix Kiprono Bett - LinkedIn](https://www.linkedin.com/in/felix-kiprono-10b19019b).
