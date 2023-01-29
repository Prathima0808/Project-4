# Movie recommendation

## Team Members: Peregrin Ryan, Anam Khalid, Prathima Polavarapu, Zitarashe Okot

##  https://github.com/Prathima0808/Project-4.git   


![everything_is_reco_800px_web](https://user-images.githubusercontent.com/110397465/213392639-60a5186b-cd73-45ba-bf35-0d90d481d294.jpg)


# Contents:

 1. [Project Overview](https://github.com/Prathima0808/Project-4/edit/main/README.md#project-overview)
 2. [About DataSet](https://github.com/Prathima0808/Project-4/edit/main/README.md#about-dataset)
 3. [Technologies](https://github.com/Prathima0808/Project-4/edit/main/README.md#technologies)
 4. [Extracting, Transforming and Loading process](https://github.com/Prathima0808/Project-4/edit/main/README.md#extracting-transforming-and-loading-process-etl)
    *  [Connecting DataSets](https://github.com/Prathima0808/Project-4/edit/main/README.md#connecting-datasets)
    *  [Transforming and Loading Data](https://github.com/Prathima0808/Project-4/edit/main/README.md#transforming-and-loading-data)
 5. [Data visualization,KNN Model](https://github.com/Prathima0808/Project-4/edit/main/README.md#data-visualizationknn-model)
    *  [Data Processing](https://github.com/Prathima0808/Project-4/edit/main/README.md#data-processing)
 6. [ Movie Recommendation using KNN](https://github.com/Prathima0808/Project-4/edit/main/README.md#movie-recommendation-using-knn-with-input-as-movie-id-and-number-of-movies-you-want-to-get-recommended)
 7. [Observasions.](https://github.com/Prathima0808/Project-4/edit/main/README.md#observasions)
 8. [Reference](https://github.com/Prathima0808/Project-4/edit/main/README.md#reference)


# Project Overview

Knowledge-based, Content-based and Collaborative Recommender systems are built on MovieLens dataset with 100836 movie ratings/reviews. These Recommender systems were
built using Pandas operations and by fitting KNN (K-Nearest Neighbours Algorithm), NCF (Neural Collaborative Filtering) & deep learning models which use NN (Neural Network) architecture to suggest movies for the users based 
on similar users and for queries specific to genre, user, movie, rating, popularity.

# About DataSet

In this Project We're used [Movie Lens](https://movielens.org/) Dataset. MovieLens is a rating dataset from the MovieLens website, 
which has been collected over some period. Stable benchmark dataset. 100836 ratings from 610 users on 9724 movies. 
Further information regarding this dataset can be found [here](https://www.kaggle.com/datasets/shubhammehta21/movie-lens-small-latest-dataset).

  This Dataset Consists of 
  * 100836 ratings from 610 users on 9724 movies.
  * Each user has rated at least 20 movies.
  * Simple info contains like( Movie Id, genre, movie Rating)

 ## Our Aim:
 
What to watch? With so many new and old movies out there we are spoiled for choice of what movies to watch next. But that choice leaves us spending more time 
looking for the next movie than actually watching it! It’s also hard to tell if we will even like the movie we settle on with just a blurb and a poster. 
Our goal is to fix this great problem of our time by creating a machine learning model that will help users find what movies to watch next based on a 
user's preferences.
 
# Getting Strated:

 To get a local copy up and running follow these simple example steps:
 
 1. Clone the reposirory by using Local Terminal Gitbash [Gitbash Terminal](https://git-scm.com/download/win)
 2. using the [Jupyter Notebook](https://jupyter.org/) in which you performed the preprocessing steps.
 
 
#### [Managing Libraries](https://pypi.org/project/pip/)

 3. sqlalchemy (SQl database)
    * conda install -c anaconda sqlalchemy
    * config
    * pip install config
 
 4. matplotlib.pyplot
 
    * pip install matplotlib
  
 5. tensorflow
    
    * pip install tensorflow
    
 6. numpy
    
    * pip install Numpy
    
 7. Scikit-learn Mechiene Learning Library




# Extracting, Transforming and Loading process (ETL)

    The data was provided to us in a CSV. We checked for any null values in the dataset, and did not have any. We also checked to verify that datatypes 
    matched the variables values as described above. Our data checked out in all these areas, so no additional transformation was required. 
    Then, we created an SQL database for our data to be stored in. We did this using our knowledge of SQL Database and Pandas.

    In this process we're extracting data into dataframe:
    
![2023-01-27 (2)](https://user-images.githubusercontent.com/110397465/214853472-faa4d030-d317-4f3a-a9a7-4c64d655acb7.png)

   ## Connecting DataSets:
   
   * Connect to the local database. Here create a config.py file and keep your username and password in it and save the config.py file in .gitignore file to keep your       username and password confidential. 
      If it's not confidential, you can put it straight away in the code and you won't have to create config.py or .gitignore file then.
 
  ![2023-01-27 (4)](https://user-images.githubusercontent.com/110397465/214854683-4c016cd1-7f95-4ce2-b19d-471241f20a4c.png)
>>>>>>> f297c66fba7fed16b973c271d9aa7dcdd9c38f07
    
   ## Transforming and Loading Data:
   
   * We're choose SQL, first use Spark on Colab to extract and transform the data and then load it into a SQL table on your RDS account. Perform analysis 
     with SQL queries on RDS.
   
   * Join two tables in pgAdmin or join the two tables in with Pandas and SQLAlchemy.
   * The two dataset are successfully loaded into an RDS instance.
   
   ![2023-01-27 (6)](https://user-images.githubusercontent.com/110397465/214855691-2d31d597-eb44-4df5-b35f-04979fd2ac36.png)
   
   
# Data visualization,KNN Model:


One flaw with the data set is that some movies are reviewed far more than others, this can cause a skewed recommendation for the data. This is a problem 
that will be addressed later in the process.


    
![2023-01-27 (8)](https://user-images.githubusercontent.com/110397465/214870182-2429c79a-efde-466d-a491-f6626c00139f.png)


Here we can see "Forrest Gump (1994)" has significantly more reviews than any other movie within the data set, whilst many other movies only have a single 
review. This is a highly skewed dataset that if left unaddressed will cause the recommendations to potentially be biassed.

# Data Processing:

The data that has now been imported needs to be processed. The 'user_id's and 'movie_id's are being enumerated as the machine learning will be more effective when the data is 0 indexed.

![2023-01-27 (10)](https://user-images.githubusercontent.com/110397465/214871911-6b71f511-beb4-4a22-9517-051d82a55f73.png)

Although the 'user_id's are not the only data we are using, we are aiming to include movies in the deep learning model as well. This means we need to enumerate the 'movie_id' so we can use them later in the process.



## Movie Recommendation using KNN with Input as Movie ID and Number of movies you want to get recommended:


  Reshaping model in such a way that each movie has n-dimensional rating space where n is total number of users who could rate.

We will train the KNN model inorder to find the closely matching similar movies to the movie we give as input and we recommend the top movies which would more closely align to the movie we have given.

For this section, a separate list for movie names and also case insensitive movie names and a dictionary which maps movie name with the index are created.

Basic output of this recommender system using KNN:
![2023-01-27 (12)](https://user-images.githubusercontent.com/110397465/214875021-e4bf1bd2-59e0-4238-afed-ccc8b256510e.png)

# Observasions:  

  
  
  
# Reference:  

* [Convolutional Neural Networks for Visual Recognition](http://cs231n.stanford.edu/)
* [KNN Explanation from Data Science Blog](https://ujjwalkarn.me/2016/08/11/intuitive-explanation-convnets/)
* [Keras documentation for the VGG19 Model](https://keras.io/api/applications/vgg/#vgg19-function)
* [Keras documentation for the Xception model](https://keras.io/applications/#xception)
* [Pyspark documentation](https://spark.apache.org/docs/latest/api/python/)









    





