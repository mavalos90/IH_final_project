# IH Final Project: Recommender System based on NLP
Repository of the Final Project in IH Data Analytics

Miguel Ángel Ávalos Barrios

*Data Part Time Barcelona Dic 2019*

## Content

**Index**   
1. [Project Description](#id1)
2. [Dataset](#id2)
3. [Work Description](#id3)
4. [Results](#id4)
5. [Sources](#id5)

<hr style="color: #7acaff;" width="50%" />

<a name="project"></a>

## Project Description<a name="id1"></a>

The main objective of this project is create a colaborative filtering recommender system based on the reviews of the customer of different restaurants using different NLP (Natural Language Processing) techniques. Therefore, various recommenders systems were constructed. First, a "classical" recommender system based exclusivetely on the ratings of the users. With these recomender as a guideline, two different recommenders were constructed using NLP. The first of them, was constructed using Sentiment Analysis as a prediction of the rating. The other one was constructed using the whole sentence using word2vector embedding.


## Dataset<a name="id2"></a>

The dataset chosen for this project is from <a href="https://www.yelp.com/dataset/">Yelp</a>. This dataset has different available information in JSON (JavaScript Object Notation) format. The two JSONs selected from the dataset were the following:

* **business.json**:

```
- *business_id*: string, 22 character unique string business id
- *name*: string, the business's name
- *address*: string, the full address of the business
- *city*: string, the city
- *state*: string, the state (if aplicable)
- *postal code*: string, the postal code
- *latitude*: float, latitude
- *longitude*: float, longitude
- *stars*: float, rounded mean of rating
- *review_count*: integer, number of reviews
- *is_open*: integer, 1 is is open
- *attributes*: object, business attributes to values
- *hours*: an dictionary of key day to value hours
``` 

* *reviews.json**:

```
- *review_id*: string, 22 character unique review id
- *user_id*: string, 22 character unique user id, maps to the user in user.json
- *business_id*: string, 22 character unique string business id
- *stars*: integer, rating 
- *date*: string date format
- *text*: string, the review itself
- *useful*: integer, number of useful votes received
- *funny*: integer, number of funny votes received
- *cool*: integer, number of cool votes received
``` 


## Workflow<a name="id3"></a>

The workflow of this project can be described into the following steps:

### Load and Selection raw data from Dataset

In order to work with the dataset, previously it was necessary to load the business (+ 3GB) and reviews (+ 6GB) and extract the information required. Only restaurants as a business type was selected, limiting the dataset size to 2.7M of rows.

### Exploratory Data Analysis
A briefly study of the main restuarant cuisines, ratings and localitations of them. 

### Preprocessing
The main task done in this step was transforming was cleaning the text, extracting the lemmas and finally tokenize it.

### Models
Differents algorithms were tested in order to create the different Recommender Systems, including kNN with pearson, cosine and msd distance, and SVD and NMF for matrix factorization. After comparing the performance of the models using RMSE (as well as MAE and MSE), a fine tunning of the different parameters was performed.

### Final Metrics

Different metrics were calculated in order to assess the recommendations of the fine tunned recommender systems, including Mean Average Precission at K=10 (MAP@10) and Mean Average Recall at K = 10 (MAR@10), as well as catalog or novelty index of the recommendations.


## Results<a name="id4"></a>
Three different Recommender Systems where constructed. NLP based recommenders performed better that the classical rating approach in the different 

## Sources <a name="id5"></a>


<hr style="color: #7acaff;" width="50%" />

<img src="https://bit.ly/2VnXWr2" alt="Ironhack Logo" width="100" align="center"/>
