# Movie recommendation

## Team Members: Peregrin Ryan, Anam Khalid, Prathima Polavarapu, Zitarashe Okot


![everything_is_reco_800px_web](https://user-images.githubusercontent.com/110397465/213392639-60a5186b-cd73-45ba-bf35-0d90d481d294.jpg)


# Contents:

    1. [About DataSet]
    2. [Technologies]
    3. [Extracting, Transforming and Loading process]
    4. []





# About DataSet

    Knowledge-based, Content-based and Collaborative systems are built on MovieLens dataset with 100,000 movie ratings. These Recommender systems were built using Pandas operations and by fitting KNN, SVD & deep learning models which use NLP techniques and NN architecture to suggest movies for the users based on similar users and for queries specific to genre, user, movie, rating, popularity.

    A recommender system is a subclass of information filtering system that seeks to predict the "rating" or "preference" a user would give to an item. Recommender systems are utilized in a variety of areas including movies, music, news, social tags, and products in general. Recommender systems typically produce a list of recommendations and there are few ways in which it can be done. Two of the most popular ways are – through collaborative filtering or through content-based filtering.

    Most internet products we use today are powered by recommender systems. YouTube, Netflix, Amazon, Pinterest, and long list of other internet products all rely on recommender systems to filter millions of contents and make personalized recommendations to their users. Recommender systems are well-studied and proven to provide tremendous values to internet businesses and their consumers.


# Requirments:

    *  Clone this repository using git clone

       https://github.com/Prathima0808/Project-4.git


    *   Install the following libraries in your local using terminal/Gitbash. You'll use these libraries later in your code for 
         the data analysis purpose.

        1. Pandas
        pip install pandas
        requests
        python -m pip install requests
        
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
<<<<<<< HEAD
=======
    

   
   
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


One flaw with the data set is that some movies are reviewed far more than others, this can cause a skewed recommendation for the data. This is a problem that will be addressed later in the process.


    






   





    





