# Fashion - Neural Network

## Intro 
You provide consulting services for an e-commerce business where customers can submit written reviews for any items they buy. By analyzing these reviews, the company can gain valuable insights into which products are popular and well-received, as well as those that are not performing as well. 

## Scenario
A crucial aspect of the online store is the collection of user reviews. Traditionally, staff members have been tasked with sifting through each review to classify them as positive, negative, or neutral. This manual process can be quite labor-intensive and inefficient, prompting the need for automation to streamline the workflow. An automated system could efficiently scan through all the reviews and, by examining the language used, assess whether the customer had a positive or negative experience with the product.

To enhance efficiency,  the aim is to implement sentiment analysis on these reviews to gauge customer opinions about products. This task falls under the umbrella of natural language processing (NLP) and can be effectively tackled by developing a recurrent neural network (RNN). By creating a review classifier powered by an RNN, sentiment evaluation process can be automated.

**Data Sources:**

- [IMDb Movie Review Dataset](https://ai.stanford.edu/~amaas/data/sentiment/) 

| LABEL | DESCRIPTION |
|-------|-------------|
| 0     | Negative Sentiment|
| 1     | Positive Sentiment|


## Project Goals
The objective is to create a sentiment evaluation system that automatically classifies reviews.


Several questions will be asked:

- How long do reviews typically average in word count?
- What is the standard deviation for the word count of reviews?
- What happens to the layer sizes as the model approaches the final outputlayer?
- How accurate is the model's performance?
- What is the moel's loss?
- What insights can you share regarding the inaccurate classifications?
- What strategies could be employ to retrain this RNN model and enhance its performance?





#### Why use a Recurrent Neural Network algorithm to predict the outcome?
The convolutional neural network previously employed are primarily feedforward neural networks (FNNs), where information travels in a single direction between layers. In contrast, recurrent neural networks (RNNs) allow for bidirectional information flow through interconnected loops. This unique capability enables RNNs to handle sequences of data, making them particularly well-suited for tasks that involve time-sensitive predictions, such as forecasting the next element in a sequence.

## Data
A dataset that can be used to train the machine-learning model has been found. This is dataset of a dataset of 25,000 IMDb records. 

## Conclusions
- How long do reviews typically average in word count?
    - Typically 239 words. 
- What is the standard deviation for the word count of reviews?
    - 176 
- What happens to the layer sizes as the model approaches the final outputlayer?
    - The sizes of the input and output can differ from one layer to another. As the final output layer is approached, which is usually a dense network, the dimensions of each preceding layer generally decrease.
- How accurate is the model's performance?
    - 86% 
- What is the moel's loss?
    - 0.45 
- What insights can be shared regarding the inaccurate classifications?
    - It's clear that the tone is negative, but there might be clues that led the model to interpret it as positive. 
- What strategies could be employ to retrain this RNN model and enhance its performance?
    - Increasing the vocabulary beyond 10,000 words or eliminating that limit entirely could supply the model with more valuable information.

        Additionally, adjusting the LSTM and dense layers to incorporate various output sizes, along with adding extra layers, might further boost the model's performance. Ultimately, the key is to thoroughly experiment with these hyperparameter settings to find the best configuration. 