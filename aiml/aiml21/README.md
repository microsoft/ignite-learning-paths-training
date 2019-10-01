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
* Use the **Deploy to Azure button** below to create your Azure Machine Learning workspace to use throughout the session: ---- deploy to azure button ----
* Log into the Azure Portal and your Azure Machine Learning Service
* Launch the **Preview UI**
* Create a **Notebook VM**
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

* Create a **Compute Instance**
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

* Upload the **Dataset**
    * Select 'Datasets' from left pane
    * Select 'Create dataset' and then 'from local files'
    * Select the 'Browse' button and find the data_train_experiment.csv file
    * Wait for the file to upload
    * Select 'Done'


## Demo 1 - Explore

Video Demo with Voice Over: [AIML21 - Demo 1 - Explore](https://youtu.be/1Xtmrsfkzfs)

**Instructions:**
* Sign into your [Azure Portal](https://azure.microsoft.com/en-gb/) and open the **Azure Machine Learning Workspace** you created with the template above
* Launch the Preview experience by clicking **'Launch Preview Now'**
* Open **'Notebook VMs'** from the left pane
* Select the **'Jupyter'** Link
* Double click the **user folder**
* *Log in if needed with your Azure Credentials*
* Open **Explore.ipynb** *(recommend having all these tabs open and ready already)*
* Make sure all output cells in the notebook are cleared - **Select Cell -> All Output -> Clear**
* **Review the video for all talking points for each demo**
* Run through and explain the first 6 cells briefly
* Note further cells and visualizations are available and attendees should download the code from **[aka.ms/AIML21repo](http://aka.ms/aiml21repo)**

## Demo 2 - Experiment

* Video Demo with Voice Over: [AIML21 - Demo 2 - Experiment](https://youtu.be/sUKuRBRvo7U)

* Go to [ml.azure.com](https://ml.azure.com/) Azure Machine Learning Preview interface. You can access this via the URL directly and then sign in and select the correct workspace you created for this talk. Or from the Azure Machine Learning Service workspace in the portal selecting the **'Launch Preview now'** button
* Select **Automated ML** on the left pane
* **Review the video for all talking points for each demo**
* Click **'Create experiment'**
* Provide an experiment name, example/ aiml21-regression-duration
* Select your Machine Learning compute you setup above
* Select **Next**
* Select the dataset you uploaded above
* Review the preview of the dataset
* **Deselect** the columns below:
    * SupportTicketID
    * CustomerID
    * DateCreated
    * DateCompleted
    * CustomerID2
    * CompletedTutorial
    * Rating
    * GeographyID2
    * RoleID2
    * DateCompletedDay
    * DateCompletedMonth
    * DateCompletedYear
* Select **Regression** for Prediction Task
* Select **Duration** for Target column
* Select **Advanced Settings** drop down
* Set Primary metric to **'normalized_root_mean_squared_error'**
* Set Training Job time (minutes) to **10**
* Select **Start** button

>> Once it is running, explain it will take some time to run the experiment and you will review a previously run example. 
>> Please make sure you have a fully run Automated ML regression as explained about before getting on stage

* Select previously run experiment from the Automated ML page from the left, or press the back button from the experiment you just submitted above
* The previously run experiment will have a long 'Run Id' select this link
* **Review the video for all talking points for each demo**

## Demo 3 - Deploy

* Video Demo with Voice Over: [AIML21 - Demo 3 - Deploy](https://youtu.be/IgSaMKsyexg)


## Demo 4 - Present

* Video Demo with Voice Over: [AIML21 - Demo 4 - Present](https://youtu.be/g7aBaC9s9qQ)



# Teardown Instructions

# Resources and Continued Learning

# Feedback Loop

All speakers will have the opportunity to attend Train-the-Trainer Q&A sessions every month (two sessions covering all timezones) and also after delivering the content on stage we would be keen for you to join us in the Feedback sessions organized to share your experience of the content and anything you would like to provide feedback or ideas on. 

Do you have a comment, feedback, suggestion? Currently, the best feedback loop for content changes/suggestions/feedback is to create a new issue on this GitHub repository. To get all the details about how to create an issue please refer to the [Contributing docs](https://github.com/microsoft/ignite-learning-paths/blob/master/contributing.md)
