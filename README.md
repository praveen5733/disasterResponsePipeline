# Disaster Response Pipeline Project
### Introduction

In this project, the pre-labeled disaster messages will be used to build a disaster response model that can categorize messages received in real time during a disaster event, so that messages can be sent to the right disaster response agency.

This project includes a web application where disaster response worker can input messages received and get classification results.

### Files in the repository
Folder: app
1. template
   - master.html # main page of web app
   - go.html # classification result page of web app
2. run.py # Flask file that runs app

Folder:data
1. disaster_categories.csv # data to process
2. disaster_messages.csv # data to process
3. process_data.py

Folder:models
1. train_classifier.py
2. classifier.pkl # saved model

README.md

### Instructions:
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Go to `app` directory: `cd app`

3. Run your web app: `python run.py`