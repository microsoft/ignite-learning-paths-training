# AIML21: Developers Guide to AI: A Data Story 

## Train-the-Trainer Guide**

### Session Abstract

In this theatre session we will show the data science process and how to apply it. From exploration of datasets to deployment of services - all applied to an interesting data story. This will also take you on a very brief tour of the Azure AI Platform.

# How to Use

Welcome, Presenter!

We're glad you are here and look forward to your delivery of this amazing content. As an experienced presenter, we know you know **HOW** to present so this guide will focus on **WHAT** you need to present. It will provide you a full run-through of the presentation created by the presentation design team.

Along with the video of the presentation, this document will link to all the assets you need to successfully present including PowerPoint slides and demo instructions & code.

* Read the document in its entirety.
* Watch the video presentation
* Ask questions of the Lead Presenter

# Assets in Train-the-Trainer Kit

* This guide
* [PowerPoint presentation](https://globaleventcdn.blob.core.windows.net/assets/aiml/AIML21_DevelopersGuidetoAI_ADataStory.pptx)
* Full-length recording of presentation
* [Datasets used](aiml21/data)
* [Code files to run](aiml21/code)
* Separate Demo Videos: 
    * Demo 1 - [Explore](https://youtu.be/1Xtmrsfkzfs)
    * Demo 2 - [Experiment](https://youtu.be/sUKuRBRvo7U)
    * Demo 3 - [Deploy](https://youtu.be/IgSaMKsyexg)
    * Demo 4 - [Present](https://youtu.be/g7aBaC9s9qQ)
* Demo Instructions

# Demo Instructions:

Please download all the code and data files in this repository to get started. There is a code and data folder which will contain all information you need to run all demos

**You will need:**
* Azure Subscription - get a [free trial here](https://azure.microsoft.com/en-gb/free) if you need it
* [Power BI Desktop (Windows Only)](https://powerbi.microsoft.com/en-us/desktop/) - if you are running on MacOS/Linux you can still demo the functionality from any modern web browser

**Setup Instructions:**
* Use the deploy to Azure button below to create your Azure Machine Learning workspace to use throughout the session: **deploy to azure button**
* Log into the Azure Portal and your Azure Machine Learning Service
* Launch the Preview UI
* Create a Notebook VM
    * Select 'Notebook VMs' from left pane
    * Select 'New'
    * Provide a 'Notebook VM Name' (all lowercase)
    * Keep the default size VM provided
    * Once created select 'Jupyter Link'
    * Enter the user folder by double clicking
    * Select the upload button and upload the files listed below:
        * [data/data_train.csv](data/data_train.csv)
        * [code/explore.ipynb](code/explore.ipynb)
        * [code/deploy.ipynb](code/deploy.ipynb)
        * [code/config.json](code/config.json)

* Create a Compute Instance
    * Select 'Compute' from left pane
    * Select 'Add'
    * Provide a 'Compute Name' (all lowercase)
    * Select 'Machine Learning Compute' as Compute type
    * Choose a VM size
        * For standard compute select something like 'Standard_DS2_v2'
        * For GPU compute select 'Standard_NC6'
    * Select 'Low Priority' for Virtual machine priority
    * Minimum number of nodes set to 0 (then it will scale down completely and reduce costs)
    * Click 'Create'

* Upload the Dataset
    * Select 'Datasets' from left pane
    * Select 'Create dataset' and then 'from local files'
    * Select the 'Browse' button and find the data_train_experiment.csv file
    * Wait for the file to upload
    * Select 'Done'


## Demo 1 - Explore

Video Demo with Voice Over: [AIML21 - Demo 1 - Explore](https://youtu.be/1Xtmrsfkzfs)

**Instructions:**
* Sign into your [Azure Portal](https://azure.microsoft.com/en-gb/) and open the Azure Machine Learning Workspace you created with the template above
* Launch the Preview experience by clicking 'Launch Preview Now'
* Open 'Notebook VMs' from the left pane
* Select the 'Jupyter' Link




## Demo 2 - Experiment

* Video Demo with Voice Over: [AIML21 - Demo 2 - Experiment](https://youtu.be/sUKuRBRvo7U)


## Demo 3 - Deploy

* Video Demo with Voice Over: [AIML21 - Demo 3 - Deploy](https://youtu.be/IgSaMKsyexg)


## Demo 4 - Present

* Video Demo with Voice Over: [AIML21 - Demo 4 - Present](https://youtu.be/g7aBaC9s9qQ)



# Teardown Instructions

# Resources and Continued Learning

# Feedback Loop

All speakers will have the opportunity to attend Train-the-Trainer Q&A sessions every month (two sessions covering all timezones) and also after delivering the content on stage we would be keen for you to join us in the Feedback sessions organized to share your experience of the content and anything you would like to provide feedback or ideas on. 

Do you have a comment, feedback, suggestion? Currently, the best feedback loop for content changes/suggestions/feedback is to create a new issue on this GitHub repository. To get all the details about how to create an issue please refer to the [Contributing docs](https://github.com/microsoft/ignite-learning-paths/blob/master/contributing.md)
