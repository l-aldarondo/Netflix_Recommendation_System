# Netflix_Recommendation_System
Build a Netflix recommendation system using Python Scikit-learn machine learning library.

## Background

### Overview of Analysis

This project consists of two technical analysis deliverables and a written report:

- Deliverable 1: Perform ETL on Netflix Movies and TV Shows 2021

- Deliverable 2: Build a Netflix Recommendation System using the Python programming language.

- Deliverable 3: A Written Report on the Analysis (README.md)


### Purpose

Netflix is a subscription-based streaming platform that allows users to watch movies and TV shows without advertisements. One of the reasons behind the popularity of Netflix is its recommendation system. Its recommendation system recommends movies and TV shows based on the user’s interest. 

In this project, we will choose one Netflix dataset, then we will use Python to perform the ETL process to extract the dataset, transform the data, load the transformed data into pgAdmin. Then, use Python Scikit-learn machine learning library, Natural Language Toolkit and Cosine similarity to build a Netflix Recommendation System.

## Resources

Data source:

- (1) Netflix_Recommendation_System_starter_code, (2) netflixData.csv

Software:

- Google Colab, Python 3.7.10, pgAdmin 6.14, Visual Studio Code 1.71.2
 
<br/>

## Methodology

### D1: Perform ETL on Amazon Product Reviews

<br/>

We chose a [Netflix dataset](https://www.kaggle.com/datasets/satpreetmakhija/netflix-movies-and-tv-shows-2021) to be analyzed.


### ETL process to extract the dataset, transform the data:

1. Now let’s import the necessary Python libraries and the dataset we need for this task:

(ba![customer_id_table](./Images/customer_id_table.png)
 
<sub> Figure (a) The customers_table DataFrame

<br/>

2. look at whether the data contains null values or not:

(b)![customer_id_table](./Images/customer_id_table.png)
 
<sub> Figure (b) The customers_table DataFrame

<br/>

3. let’s select the columns that we can use to build a Netflix recommendation system:

(c)![customer_id_table](./Images/customer_id_table.png)
 
<sub> Figure (c) The customers_table DataFrame

<br/>

4. Now let’s drop the rows containing null values using dropna() function.

(d)![customer_id_table](./Images/customer_id_table.png)
 
<sub> Figure (d) The customers_table DataFrame

<br/>

5. Now I will clean the Title column as it contains some data preparation using NTLK library:

(e)![customer_id_table](./Images/customer_id_table.png)
 
<sub> Figure (e) The customers_table DataFrame

<br/>

6. let’s have a look at some samples of the Titles:

(f)![customer_id_table](./Images/customer_id_table.png)
 
<sub> Figure (f) The customers_table DataFrame

<br/>

7. use the Genres column as the feature to recommend similar content to the user. I will use the concept of cosine similarity:

(g)![customer_id_table](./Images/customer_id_table.png)
 
<sub> Figure (g) The customers_table DataFrame

<br/>

8. set the Title column as an index so that we can find similar content by giving the title of the movie or TV show as an input:

(h)![customer_id_table](./Images/customer_id_table.png)
 
<sub> Figure (h) The customers_table DataFrame

<br/>


### The products_table DataFrame:

To create the products_table, we used the select() function to select the product_id and product_title, then droped duplicates with the drop_duplicates() function to retrieve only unique product_ids.


(c)![product_id_table](./Images/product_id_table.png)
 
<sub> Figure (c) The final products_table DataFrame

<br/>

### The review_id_table DataFrame:

To create the review_id_table, we used the select() function to select the columns that are in the review_id_table in pgAdmin and convert the review_date column to a date.


(d)![review_id_table](./Images/review_id_table.png)
 
<sub> Figure (d) The final review_id_table DataFrame

<br/>

### The vine_table DataFrame:

To create the vine_table, we used the select() function to select only the columns that are in the vine_table in pgAdmin


(e)![vine_table](./Images/vine_table.png)
 
<sub> Figure (e) The final vine_table DataFrame

<br/>

### D2:Determine Bias of Vine Reviews

1. write a function to recommend Movies and TV shows on Netflix:

(i)![customer_id_table](./Images/customer_id_table.png)
 
<sub> Figure (i) The customers_table DataFrame

<br/>


## Results:





## Summary

The recommendation system of Netflix predicts a personalised catalogue for you based on factors like your viewing history, the viewing history of other users with similar tastes and preferences, and the genres, category, descriptions, and more information of the content you watched.


## References

[Markdown](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

[Dataset](https://www.kaggle.com/datasets/satpreetmakhija/netflix-movies-and-tv-shows-2021)

[Starter_code](https://thecleverprogrammer.com/2022/07/05/netflix-recommendation-system-using-python/)

[Cosine Similarity in ML](https://thecleverprogrammer.com/2021/02/27/cosine-similarity-in-machine-learning/)
 
[Google Colab](https://colab.research.google.com/github/jakevdp/PythonDataScienceHandbook/blob/master/notebooks/01.01-Help-And-Documentation.ipynb)

