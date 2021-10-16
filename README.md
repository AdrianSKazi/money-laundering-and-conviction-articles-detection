# money-laundering-and-conviction-articles-detection

## Data science interview task:

<i>Please provide a model, which can classify whether a news piece describes money laundering

activity or not. Also, if it does, please provide info whether it is in allegations/accusations/charges or conviction/sentencing context.


You will need to compile the necessary training data yourself. However, the data size can be small (10-20 examples is sufficient), but diverse enough to demonstrate the model’s workings. 

Given the short timeframe you can limit the scope of the task as you see fit. However, you will

be asked to justify each constraint later on.


The code for the solution should be developed in Python and delivered as a script or jupyter

notebook. You'll be evaluated on code quality and logic clarity but not on accuracy. Please provide the code and any additional artifacts you may generate in a single zip file.


Deadline: You will have 7 business days to complete the task.</i>

--------------------------------
------------

Application created for money laundering articles detection, then from positive detection of whether conviction or allegation.

*The aim of this model is not to achieve high accuracy but to present way of 
solving mentioned problem. Accuracy probably will be low due to small amount of articles for training and it's labels.*


Below model ought to predict whether the article is about money laundering activity or not. Then if it is model will predict whether the article is in tone of allegations or convictions.

To make it work I will use 2 models trained on 2 separate datasets.
* 1 dataset is assembled of 25 articles about money laundering and other subjects articles. Thats how model will learn how to distinguish money laundering article from the others. All variables' names belonging to this model start from 'ml' from Money Laundering.
* 2 dataset is assembled of 20 articles with allegations or convictions. Thats how model will learn how to distinguish convictions from allegations. All variables' names belonging to this model start from 'ind' from Indictment.

After creating two separate models I will use them accordingly on the new articles df assembled from articles without labels. Thus, ml_model will be launched on the articles df first to filter out money activity articles only, creating ml_model df. Subsequently ind_model will separate allegations articles and conviction articles from ml_mode df, creating final ind_model df. All can be run through Application.
