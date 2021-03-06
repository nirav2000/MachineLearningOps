# Introduction to Machine Learnin Operationalization using Azure Machine Learning Services
This series of labs introduces core features of Azure Machine Learning (AML) service and demonstrates how AML service can be used to orchestrate machine learning workflows. The labs walk you through the key phases of a machine learning workflow: from data preparation, through model selection and tuning, to model operationalization. It concludes with a lab on Automated Machine Learning. There is an optional Model Interpretability lab which you can run through as well.



## Lab environment set up

The Azure Machine Learning service is platform agnostic. The only requirements for your development environment are Python 3, Conda (for isolated environments), and a configuration file that contains your Azure Machine Learning workspace information.

The following development environments are supported: 
- **Azure Notebooks**
- **The Data Science Virtual Machine**
- **Jupyter Notebooks**
- **Visual Studio Code**
- **Visual Studio**
- **PyCharm**
- **Azure Databricks**

However, for the purpose of this lab we will set up your lab environment in your local machine (PC or Laptop). These are the pre-requisites in terms of software and libraries in order to execute each of these labs:

Windows/Mac/Linux:
 
- **Please make sure you have the latest version of Anaconda installed https://www.anaconda.com/distribution/#download-section**
- **Install the following libraries**
 - ***pip install --upgrade azureml-sdk[explain,automl]***
 - ***pip install azureml-widgets***

For Windows users (additional steps below):

- **Install git https://github.com/git-for-windows/git/releases/download/v2.21.0.windows.1/Git-2.21.0-64-bit.exe**
- **Install wget http://downloads.sourceforge.net/gnuwin32/wget-1.11.4-1-setup.exe**
- **Make sure to add wget to your Path environment variables**

For Mac users (additional steps below):

- **Install wget: brew update && brew install wget** 

## Clone this GitHub repository locally

#From https://help.github.com/en/articles/cloning-a-repository

Open Git Bash.

Change the current working directory to the location where you want the cloned directory to be made.

Type git clone, and then paste the URL you copied in Step 2.

$ git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY  #https://github.com/nirav2000/MachineLearningOps.git

## Install AMLSDK for Python

https://docs.microsoft.com/en-us/python/api/overview/azure/ml/install?view=azure-ml-py

pip install --upgrade azureml-sdk

## Open Jupyter Notebook

- In CMD/PoweShell (maybe with Admin rights)
- move into the clone GitHub directory
- run: jypter notebook (should load notebook in browser or give a url) #if it doesn't work it may be because it cant find anaconda, either make sure its setup in your system environment variables or type out full directory of where jypter is located

## Redeem your Azure account promo code

The steps below outline how you can redeem your promo code and create your new Azure account. However, if you already have an Azure account please feel free to use that as that is the preferred option. Alternatively, follow the steps below to create a new one using the promo codes we have provided you. Note, the accounts with the promo code will expire after 7 days and they come with a $50 limit.

1. You need to have an .outlook or .live account. Please create one if you don't have it.
2. Then follow the instructions here to redeem your promo code and create your Azure account: https://www.microsoftazurepass.com/Home/HowTo


## Create Azure Machine Learning service workspace

Once you have access to an Azure account follow the steps below to create an Azure Machine Learning workspace.

1. In your Azure portal, click **Create a resource**
2. In the **Search the Marketplace** textbox, type: ***Machine Learning*** and select **Machine Learning service workspace** from the drop down list.
3. In the next screen click the button **Create**
4. You only need to fill Workspace name, Resource group, and Location.
5. For **Workspace name** give it a name (e.g. MLOpsYourName)
6. For **Resource group** give it a name (e.g. MLOpsYourNameRGR)
7. For **Location** please select: West Europe
8. Click the button **Create** to create the Machine Learning workspace

### AML workspace information needed for the labs jupyter notebook

Once the Azure Machine Learning workspace has been created, please click on the AML Service in the Azure portal and capture the following information which you will use in a labs Jupyter Notebook.
- **Subscription ID**
- **Location**
- **Resource group**
- **Workspace name** which is just the name of the AML service

You will use this information in the **00-AML-Workspace-Setup / 00-setup** jupyter notebook

### (Optional) Model Interpretabiltiy / Explainability

Model interpretability and explainability is becoming increasinly important in the Machine Learning world. Microsoft has baked in model interpreatibility and explainability features in its Azure Machine Learning service and you can try this out now. 

1. Read the following introduction on Azure Machine Learning Interpretability SDK: https://docs.microsoft.com/en-us/azure/machine-learning/service/machine-learning-interpretability-explainability
2. Try out the Jupyter Notebook examples listed in the above link.

