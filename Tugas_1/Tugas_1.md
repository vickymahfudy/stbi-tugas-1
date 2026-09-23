# Assignment: Information Retrieval Models — Vector Space and Probabilistic Approaches

# Background

In this assignment, you will build and compare several approaches to ranked retrieval, moving from traditional vector space models to probabilistic language models. You will implement tf, tf-idf, and word2vec/doc2vec representations, and then explore query-likelihood language models with smoothing (Laplace and linear interpolation), evaluating all approaches on the same dataset and queries.

# Dataset

Use the news dataset available at [this link](https://drive.google.com/file/d/13UUj240WKjosQnLfnveMcOutd0OYxBDF/view?usp=sharing). Use the text under the "content" column as your document corpus throughout the assignment.

# Objectives

* Create ranked retrieval models using tf, tf-idf, and word2vec (or doc2vec, using a pretrained model) representations.  
* Implement probabilistic query-likelihood language models for information retrieval, including Laplace (add-one) smoothing and linear interpolation smoothing.  
* Compare the vector space models against the language modeling approaches.  
* Analyze the impact of smoothing and text normalization (stemming, stopword removal, lowercasing) on retrieval performance.

# Tasks

## 1\. Data Preparation

* Load the dataset and preprocess the text under the "content" column.  
* Implement basic preprocessing (tokenization, lowercasing).  
* Create a vocabulary of unique terms.

## 2\. Build the Retrieval Models

* Vector space models: tf representation, tf-idf representation, and word2vec/doc2vec (pretrained).  
* Basic Query-Likelihood Model: query-likelihood retrieval without smoothing.  
* Laplace Smoothing: query-likelihood model with Laplace (add-one) smoothing.  
* Linear Interpolation Smoothing: query-likelihood model with linear interpolation smoothing.

## 3\. Testing and Evaluation

* Define 5 different queries and use the same set of queries across all five models (tf, tf-idf, word2vec/doc2vec, basic query-likelihood, Laplace-smoothed, linear-interpolation-smoothed).  
* For each query, retrieve the top 10 documents using each model.  
* Record the computation time for each model.  
* Evaluate whether the retrieved documents are relevant to the queries.  
* Compare the top 10 retrieved documents across all models for each of the 5 queries.

## 4\. Enhancement

* Apply the best-performing model with normalization (stemming, stopword removal, lowercasing) and evaluate whether this improves or worsens performance.  
* Optional: Implement stemming and stopword removal for the language models as well, and compare performance with and without these enhancements.

# Report

Write a report (minimum 1 page, maximum 2 pages) that provides analysis on:

* Computation time across all models.  
* The relevance of retrieved documents to each query.  
* A comparison of the top 10 ranked documents across models, for each of the 5 queries.  
* The effect of smoothing (for the language models) and normalization (stemming, stopword removal, lowercasing) on retrieval performance.

# Materials to Submit

* Code (notebook or link to the notebook).  
* Report (min 1 page, max 2 pages).