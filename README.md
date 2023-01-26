# Movie recommendation

## Team Members: Peregrin Ryan, Anam Khalid, Prathima Polavarapu, Zitarashe Okot

##  https://github.com/Prathima0808/Project-4.git   


![everything_is_reco_800px_web](https://user-images.githubusercontent.com/110397465/213392639-60a5186b-cd73-45ba-bf35-0d90d481d294.jpg)


# Contents:

 1. [Project Overview](https://github.com/Prathima0808/Project-4/edit/main/README.md#project-overview)
 2. [Technologies](https://github.com/Prathima0808/Project-4/edit/main/README.md#technologies)
 3. [Extracting, Transforming and Loading process](https://github.com/Prathima0808/Project-4/edit/main/README.md#extracting-transforming-and-loading-process-etl)
    *  [Connecting DataSets](https://github.com/Prathima0808/Project-4/edit/main/README.md#connecting-datasets)
    *  [Transforming Data](https://github.com/Prathima0808/Project-4/edit/main/README.md#transforming-data)
 4. [Data visualization,KNN Model](https://github.com/Prathima0808/Project-4/edit/main/README.md#data-visualizationknn-model)
    *  [Data Processing](https://github.com/Prathima0808/Project-4/edit/main/README.md#data-processing)
 5. [ Movie Recommendation using KNN](https://github.com/Prathima0808/Project-4/edit/main/README.md#movie-recommendation-using-knn-with-input-as-movie-id-and-number-of-movies-you-want-to-get-recommended)
 6. [Observasions.](https://github.com/Prathima0808/Project-4/edit/main/README.md#observasions)






# Project Overview

    Knowledge-based, Content-based and Collaborative Recommender systems are built on MovieLens dataset with 100,000 movie ratings. 
    These Recommender systems were built using Pandas operations and by fitting KNN, SVD & deep learning models which use NLP techniques 
    and NN architecture to suggest movies for the users based on similar users and for queries specific to genre, user, movie, rating, popularity.

   
# Technologies:

    *   Install the following libraries in your local using terminal/Gitbash. You'll use these libraries later in your code for 
         the data analysis purpose.

        1. [Pandas](https://www.anaconda.com/products/distribution)
        2. [Git Bash] (https://git-scm.com/download/win)
        3. 
        
        standard library of python so no need to download it

        2. sqlalchemy
        conda install -c anaconda sqlalchemy
        config
        pip install config

        3. Scikit-learn Mechiene Learning Library

        4. Additional: CSS, HTML, Python, Pandas, SKLearn, Bootstrap, PostgreSql, Jupyter Notebook



# Extracting, Transforming and Loading process (ETL)

    The data was provided to us in a CSV. We checked for any null values in the dataset, and did not have any. We also checked to verify that datatypes matched the variables values as described above. Our data checked out in all these areas, so no additional transformation was required. Then, we created an SQLite database for our data to be stored in. We did this using our knowledge of SQLite and Pandas.

    In this process we're extracting data into dataframe:
    
![2023-01-27 (2)](https://user-images.githubusercontent.com/110397465/214853472-faa4d030-d317-4f3a-a9a7-4c64d655acb7.png)

   # Connecting DataSets:

    * Connect to the local database. Here create a config.py file and keep your username and password in it and save the config.py file in .gitignore file to keep your       username and password confidential. 
      If it's not confidential, you can put it straight away in the code and you won't have to create config.py or .gitignore file then.
 
  ![2023-01-27 (4)](https://user-images.githubusercontent.com/110397465/214854683-4c016cd1-7f95-4ce2-b19d-471241f20a4c.png)
>>>>>>> f297c66fba7fed16b973c271d9aa7dcdd9c38f07
    
   # Transforming Data:
   
   * Join the two tables in pgAdmin or join the two tables in with Pandas and SQLAlchemy.
   
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

  An interesting observation would be that the above KNN model for movies recommends movies that are produced in very similar years of the input movie. However, the cosine distance of all those recommendations are observed to be actually quite small. This might be because there are too many zero values in our movie-user matrix. With too many zero values in our data, the data sparsity becomes a real issue for KNN model and the distance in KNN model starts to fall apart.









    





