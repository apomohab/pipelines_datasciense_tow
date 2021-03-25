## Project Overview

In this course, you've learned and built on your data engineering skills to expand your opportunities and potential as a data scientist. In this project, you'll apply these skills to analyze disaster data from Figure Eight to build a model for an API that classifies disaster messages.

In the Project Workspace, you'll find a data set containing real messages that were sent during disaster events. You will be creating a machine learning pipeline to categorize these events so that you can send the messages to an appropriate disaster relief agency.

Your project will include a web app where an emergency worker can input a new message and get classification results in several categories. The web app will also display visualizations of the data. This project will show off your software skills, including your ability to create basic data pipelines and write clean, organized code!




## Project Components
* There are three components you'll need to complete for this project.


1. ETL Pipeline

In a Python script, process_data.py, write a data cleaning pipeline that:

- Loads the messages and categories datasets
- Merges the two datasets
- Cleans the data
- Stores it in a SQLite database




2. ML Pipeline

* In a Python script, train_classifier.py, write a machine learning pipeline that:

- Loads data from the SQLite database
- Splits the dataset into training and test sets
- Builds a text processing and machine learning pipeline
- Trains and tunes a model using GridSearchCV
- Outputs results on the test set
- Exports the final model as a pickle file





3. Flask Web App

We are providing much of the flask web app for you, but feel free to add extra features depending on your knowledge of flask, html, css and javascript. For this part, you'll need to:


- Modify file paths for database and model as needed
- Add data visualizations using Plotly in the web app. One example is provided for you



### the libraries used in project 

- pandas
- sklearn
- nltk
- sqlalchemy
- pickle
- Flask
- plotly
- sqlite3
- json



## Deployment

I'm using [digitalocean](https://www.digitalocean.com/) (free tier available) to host this site. See their simple guide to ["Setting up Flask applications on digitalocean"](https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-app-using-gunicorn-to-app-platform).


## Built With

- [Flask](https://flask.palletsprojects.com/en/1.1.x/) - The web application framework used
- [Plotly](https://plotly.com/python/) - For data visualization
- [NLTK](https://www.nltk.org/) - Natural Language Toolkit for text processing methods
- [Scikit-Learn](https://scikit-learn.org/) - Python machine learning library
- [SQLAlchemy](https://www.sqlalchemy.org/) and [SQLite](https://sqlite.org) - SQL toolkit and databse engine
- [Appen (formerly FigureEight)](https://appen.com/) - Training data source
- [PythonAnywhere](https://www.pythonanywhere.com/) - Cloud platform used for deployment


## Train New Data

It is possible to use the repository to train a new dataset although you will need to follow a strict schema. The training data should be separated into two separate CSV files: a messages dataset of exactly four columns and a target labels dataset with any number of columns.

1. Run the following commands in the project's root directory to set up your database and model.

   - To run ETL pipeline that cleans data and stores in database

     ```cli
       python data/process_data.py [path/to/messages.csv] [path/to/categories.csv] [/path/to/database.db]
     ```

     For example, in the current repo, you can run `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`

   - To run ML pipeline that trains classifier and saves
     `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

1. Run the following command in the app's directory to run your web app.
   `python app/run.py`

for see the project in local computer go to the link .

1. Go to http://0.0.0.0:3001/ or [localhost:3001](http://localhost:3001/)



- for see thr project online you can go the link .

- http://174.138.124.187


