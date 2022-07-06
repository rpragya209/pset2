Abstract :
Simple Machine Learning model taking into account 6 parameters to predict if a student is having any chance of admission for MS.

Model used : RandomForestClassifier
The ML model is trained by a dataset from Kaggle.
Deployment is done through Flask, Github actions and Heroku.
The project template is cloned from cookiecutterand pushed to a newly created git repository.

DVC Pipeline creation :
dvc is initialized and dvc.yaml is populated with the stages.
In this project the stages are : load data, split data , train data and model selection.
Load data script is used to extract the required dataset from the raw dataset depending on our parameters required.
Split data script is splitting the dataset into train and test dataset which is used by model train script to train the ML model.
Depending on the accuracy, the model selection script selects the best model.

A webapp is created using Flask which consumes our ML model. Once the user enters the 6 parameters required, the Model will predict the outcome.
Javascript codes are inside the webapp folder.

Deployment :
Heroku is used to deploy the application. It is connected to the Github repository and deploys automatically everytime there is a git build.
CI CD pipeline is created using Github actions. We just need to push the code after doing the modifications and it will reflect the changes automatically.
To connect Heroku to Git, secrets are created < Heroku api name and heroku api token > .
Deployment status can be checked from the actions tab in Github.

