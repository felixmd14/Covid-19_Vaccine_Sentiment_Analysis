# Covid--19-Vaccine-Sentiment-Analysis
COVID VACCINE SENTIMENT ANALYSIS
This project aims to develop a Machine Learning model to assess positive, negative, or neutral Twitter posts related to vaccinations. The solution will help the governments and other public health actors monitor public sentiment towards COVID-19 vaccinations and help improve public health policy, vaccine communication strategies, and vaccination programs worldwide. In this project, we are working with text data; text data is initially non-numerical and must be processed before it can be fed into a Machine Learning algorithm.

For this we use Natural Language Processing - Natural language processing (NLP) is the ability of a computer program to understand human language as it is spoken and written -- referred to as natural language.

Sentiment Analysis
Sentiment analysis is the process of analyzing digital text to determine if the emotional tone of the message is positive, negative, or neutral Today, companies have large volumes of text data like emails, customer support chat transcripts, social media comments, and reviews. Sentiment analysis tools can scan this text to automatically determine the author’s attitude towards a topic. Companies use the insights from sentiment analysis to improve customer service and increase brand reputation.
Sentiment Analysis Using Hugging Face
Hugging Face is an open-source and platform provider of machine learning technologies. You can use install their package to access some interesting pre-built models to use them directly or to fine-tune (retrain it on your dataset leveraging the prior knowledge coming with the first training), then host your trained models on the platform, so that you may use them later on other devices and apps.

Please, go to the website and sign-in to access all the features of the platform.

Read more about Text classification with Hugging Face

The Hugging face models are Deep Learning based, so will need a lot of computational GPU power to train them.

Application of Hugging Face Text classification model Fune-tuning
Read more about the fine-tuning concept : here.research.google.com/) to do it, or your other GPU cloud provider, or a local machine having NVIDIA GPU.

Data Description
The data comes from tweets collected and classified through Crowdbreaks.org [Muller, Martin M., and Marcel Salathe. "Crowdbreaks: Tracking Health Trends Using Public Social Media Data and Crowdsourcing." Frontiers in public health 7 (2019).]. Tweets have been classified as pro-vaccine (1), neutral (0) or anti-vaccine (-1). The tweets have had usernames and web addresses removed.

The objective of this challenge is to develop a machine learning model to assess if a twitter post that is related to vaccinations is positive, neutral, or negative.

Data Understanding:
Here we check the data’s quality and completeness and explore variables and their relationship.

We are provided with 4 different kinds of files:

variable_definitions.csv - This file describes the different variables in the data.
sampleSubmission.csv - This file shows the structure of your submission file.
train.csv - This file contains relevant data/variables that will help train the final model; It can be split into train and test to test locally.
CaptureSite_category.csv - This file contains the capture sites and their category.
Hint: Since this is a sentiment analysis challenge we’ll likely prioritize the textual variables.

For this challenge it seems we are working with 4 different variables:

tweet_id: Unique identifier of the tweet

safe_tweet: Text contained in the tweet. Some sensitive information has been removed like usernames and urls

label: Sentiment of the tweet (-1 for negative, 0 for neutral, 1 for positive)

agreement: The tweets were labeled by three people. Agreement indicates the percentage of the three reviewers that agreed on the given label. You may use this column in your training, but agreement data will not be shared for the test set.

Files available for download are:

Train.csv - Labelled tweets on which to train your model

Test.csv - Tweets that you must classify using your trained model

SampleSubmission.csv - is an example of what your submission file should look like. The order of the rows does not matter, but the names of the ID must be correct. Values in the 'label' column should range between -1 and 1.

NLP_Primer_twitter_challenge.ipynb - is a starter notebook to help you make your first submission on this challenge.

Setup
Install the required packages to be able to run the evaluation locally.

You need to have Python3 on your system. Then you can clone this repo and being at the repo's root (root :: repo_name> ...) follow the steps below:

Windows:

  python -m venv venv; venv\Scripts\activate; python -m pip install -q --upgrade pip; python -m pip install -qr requirements.txt  
Linux & MacOs:

  python3 -m venv venv; source venv/bin/activate; python -m pip install -q --upgrade pip; python -m pip install -qr requirements.txt  
The both long command-lines have a same structure, they pipe multiple commands using the symbol ; but you may manually execute them one after another.

Create the Python's virtual environment that isolates the required libraries of the project to avoid conflicts;
Activate the Python's virtual environment so that the Python kernel & libraries will be those of the isolated environment;
Upgrade Pip, the installed libraries/packages manager to have the up-to-date version that will work correctly;
Install the required libraries/packages listed in the requirements.txt file so that it will be allow to import them into the python's scripts and notebooks without any issue. NB: For MacOs users, please install Xcode if you have an issue.
Bert Model
Bidirectional Encoder Representations from Transformers (BERT) is a state of the art model based on transformers developed by google. It can be pre-trained and later fine-tuned for a specific task.

Bert was pre-trained on the BooksCorpus dataset and English Wikipedia. It obtained state-of-the-art results on eleven natural language processing tasks.

Bert was trained on two tasks simultaneously

Masked language modelling (MLM) — 15% of the tokens were masked and was trained to predict the masked word
Next Sentence Prediction(NSP) — Given two sentences A and B, predict whether B follows A BERT is designed to pre-train deep bidirectional representations from an unlabeled text by jointly conditioning on both left and right context in all layers.As a result, the pre-trained BERT model can be finetuned with just one additional output layer to create state-of-the-art models for a wide range of tasks, such as question answering and language inference, without substantial task-specific architecture modifications.
BERT has several variants, including “bert-base-uncased” and “bert-base-cased,” which differ in their tokenization strategies (whether text is lowercase or case-sensitive), and there are larger versions of BERT with more parameters for even better performance.

Feedback and Support
Email: manureservations@gmail.com LinkedIn : linkedin.com/in/emmanuel-koech-a223a2171/ GitHub Issues: Feel free to create an issue in the GitHub repository.

Author
Emmanuel Koech
