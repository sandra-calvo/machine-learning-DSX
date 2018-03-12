# Building models with IBM Watson Machine Learning

Test application using Watson Machine Learning on Data Science Experience, running on IBM Cloud.

IBM Machine Learning: IBM Watson Machine Learning is an IBM Cloud service that enables users to perform two fundamental operations of machine learning: training and scoring.

    Training is the process of refining an algorithm so that it can learn from a data set. The output of this operation is called a model. A model encompasses the learned coefficients of mathematical expressions.
    Scoring is the operation of predicting an outcome by using a trained model. The output of the scoring operation is another data set containing predicted values.

IBM Watson Machine Learning is designed to address the needs of two primary personas:

    Data Scientists: Create machine learning pipelines that leverage data transformations and machine learning algorithms. They typically use notebooks or external tools to train and evaluate their models. Data scientists often collaborate with Data engineers to explore and understand the data.
    Developers: Build intelligent applications that use the predictions output by machine learning models.

Although training is a critical step in the machine learning process, IBM Watson Machine Learning enables you to streamline the functioning of your models by deploying them and getting actual business value from them over time and through all of their iterations.

IBM Data Science Experience

Spark

Cloud Storage


#### Pre-requisites:
  - IBM Cloud Account -  www.bluemix.net
  
## Step 1: Set up the environment on IBM Cloud

Login to www.bluemix.net and create the following services:
    - Watson Machine Learning
    - Cloud Object Storage
    - Apache Spark

In order to do so, go to the Catalog find the wanted service. 
![](/screenshots/Picture3.png?raw=true)

Watson Machine Learning service is under the Data & Analytics category. Select the service and click on create. 
![](/screenshots/Picture4.png?raw=true)

![](/screenshots/Picture7.png?raw=true)

Go back to the Catalog and repeat the process for Apache Spark also located under Data & Analytics
![](/screenshots/Picture5.png?raw=true)

![](/screenshots/Picture8.png?raw=true)

Go back to the Catalogue and repeat the process for Cloud Object Storage, located under Storage.
![](/screenshots/Picture6.png?raw=true)

![](/screenshots/Picture9.png?raw=true)

Once you have created the three services click on the IBM Cloud logo on the top left corner to go to your Dashboard. 
![](/screenshots/Picture10.png?raw=true)

Listed you will find the needed services as shown in the image.

![](/screenshots/Picture11.png?raw=true)

## Step 2: Configure Data Science Experience 

Go to https://eu-gb.datascience.ibm.com to access IBM Data Science Experience. 

![](/screenshots/Picture1.png?raw=true)

Sign in using your IBM Cloud credentials. 


## Step 3: Build and train a model
Build a logistic regression model

You can use the IBM Data Science Experience model builder to create a model automatically or manually.

#### Automatic model creation

You can create models by using IBM Data Science Experience in different ways. From within a project, when you use the Add to project > Model function, you have two choices: automatic or manual. For the automatic method, you rely on automatic data preparation (ADP) completely. For the manual method, in addition to some functions that are handled by the ADP transformer, you can add and configure your own estimators, which are the algorithms used in the analysis. 

To create a model by using the automatic model builder, perform the following steps:

    Open a project in Data Science Experience.
    If your data is not already part of the project, add a data set to the data assets for the project.
    To create a model, from the project overview page, click Add to project, and then click Model.
    Name the model.
    If you have more than one configured, you have the option to choose a machine learning service and a spark service. If you have not already configured a machine learning instance, you are prompted to assign one to this project or create one.
    To prepare your data and create a model automatically, click Automatic and then click Create.
    On the Select data asset step, select a data asset and click Next. If you don't see the data asset you wanted, you can add it from this window by clicking Add Data Assets. Not sure? Click the name of the data asset to preview it. You can also add a connection. Select connections details and click Continue. Based on your data you must select additional connection details, such as schema and table.
    After the data is loaded, you must select a column value to predict and a technique. Although a technique is automatically chosen for you, you have the option to change this.
    Optionally, adjust the validation split. By default this is set to Train: 60%, Test 20%, and Holdout: 20%.
    After you are done making adjustments, click Next.
    After the model is done training, click Save, and then, click Save again.
    If you are ready to deploy this model, from the model information page, click Add Deployment. Deploying the model makes it available to a wider audience. Note: You can have only one deployment per model. For more information, see Deploying a model.

#### Manual model creation

To create a model by using the manual model builder, perform the following steps:

    Open a project in Data Science Experience.
    If your data is not already part of the project, add a data set to the data assets for the project.
    To create a model, from the project overview page, click Add to project, and then click Model.
    Name the model.
    If you have more than one configured, you have the option to choose a machine learning service and a spark service. If you have not already configured a machine learning instance, you are prompted to assign one to this project or create one. For more information about configuring your services, see Setting up your machine learning environment.
    To prepare your data and create a model manually, click Manual and then click Create.
    On the Select data asset step, select a data asset and click Next. If you don't see the data asset you wanted, you can add it from this window by clicking Add Data Assets. Not sure? Click the name of the data asset to preview it. You can also add a connection. Select connections details and click Continue. Based on your data you must select additional connection details, such as schema and table.
    After the data is loaded, you must select a column value to predict and a technique. A suggested technique is automatically chosen for you.
    Click Add Estimators to select an algorithm to use in the analysis.
    Optionally, adjust the validation split. By default this is set to Train: 60%, Test 20%, and Holdout: 20%.
    After you are done making adjustments, click Next.
    After the model is done training, click Save, and then, click Save again.
    If you are ready to deploy this model, from the model information page, click Add Deployment. Deploying the model makes it available to a wider audience. Note: You can have only one deployment per model. For more information, see Deploying a model.

## Step 4: Deploy a model

After you create, train, and evaluate a model, you can deploy it. Although it is possible to score a model without deploying it, a model has to be deployed before it can be scored from the Watson Machine Learning APIs. Also, a model can only have a single deployment. For a trial account, a user can have only one deployed model at a time.

When you deploy a model you save it to the model repository that is associated with your Watson Machine Learning service. Then, you can use your deployed model to score data and build an application.

    Deploy a model from a notebook
    Deploy a Spark model from Flow Editor
    Deploy an IBM SPSS Model from Flow Editor
    Deploy a model from the model builder
    Deploy a model from the project
    Deploy models from IBM Watson Machine Learning on IBM Cloud
    Set up deployment for a batch or streaming model


## Step 5: Test your model 


You can create a machine learning model by using the model builder, the flow editor, or a notebook to prepare data, train the model, and deploy the model. You build your model by selecting the data, then manipulating the data, and selecting estimators or algorithms to use for classification. You can transform the data by appending new columns or mapping existing data to a new column. An estimator trains the data and produces a model, which you can deploy and use for prediction.

Before you can create a model, you must have a spark service and a machine learning service. If you don't already have a machine learning service, you are given a link and directed to create one during the initial model creation step. 
