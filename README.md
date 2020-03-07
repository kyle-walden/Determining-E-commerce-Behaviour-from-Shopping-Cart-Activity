# Determining Customer Cart Checkout based on E-Commerce Behaviour
**Project Report**

## Abstract
This project utalizes machine learning to develope a classification model to classify whether a e-commerce store visitor will proceed to purchase a product placed within their shopping cart or select to remove the product from their shopping cart - ultimetly classifying the user as a 'buyer' or 'non-buyer' for a paticular product prior to them taking action in the shopping cart. The concluding model producing the best results was a K-Nearest Neighbour (KNN) model, reporting a 70.64% accuracy rate.

## Introduction
In today's internet age, typical e-commerce online stores are able to track user activity and compile relational databases. Popular tools are used to do so such as Google Analytics - providing insights into site visitor behaviours at a detailed view point. In such, a site can easily setup a collection to track the activity that happens within a paticular users' shopping cart per browsing session.

**This document outlines topics of the model's methodology, modelling tools and techniques, and provides a summary of results and final discussion points. For a detailed code repository, please see attached Jupyter Notebook.**

## Methodology
### Dataset and Pre-processing
The data was obtained from [here](https://www.kaggle.com/mkechinov/ecommerce-events-history-in-cosmetics-shop). The raw data consists of 9 data columns. The dataset's raw relational composition is as follows:
* event_time: Time when event happened at (in UTC).
* event_type: view - a user viewed a product; cart - a user added a product to shopping cart; removefromcart - a user removed a product from shopping cart; purchase - a user purchased a product. Typical funnel: view => cart => purchase.
* product_id: ID of a product
* category_id: Product's category ID
* category_code: Product's category taxonomy (code name) if it was possible to make it. Usually present for meaningful categories and skipped for different kinds of accessories.
* brand: Downcased string of brand name. Can be missed.
* price: Float price of a product. Present.
* user_id: Permanent user ID.
* user_session: Temporary user's session ID. Same for each user's session. Is changed every time user come back to online store from a long pause.

Data pre-processing was key to prepare the data for the classification models. Feature Engineering was also vital in transforming  categorical features in the raw dataset into binary classification vairables, as well as creating time vairables for given event time feature.

### Modelling
The programming language of choice was Python. Numerous libraries were used throughout the coding script, namely Pandas, NumPy, Scikit-Learn, Seaborn, and Matplotlib. 

Classification models used to fit the data and produce predictions were: [Logistic Regression](https://en.wikipedia.org/wiki/Logistic_regression), [K-Nearest Neighbour](https://en.wikipedia.org/wiki/K-nearest_neighbors_algorithm), [XGBoost Classifier](https://machinelearningmastery.com/gentle-introduction-xgboost-applied-machine-learning/) (click on each to read on more about how the model operates).

## Results
The best performing model was a K-Nearest Neighbour (KNN), reporting a 70.64% accuracy rate. The below plot reports the accuracy of each model:



