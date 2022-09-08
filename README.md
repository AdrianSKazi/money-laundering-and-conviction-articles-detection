# money-laundering-and-conviction-articles-detection

## Model description

Application created for money laundering articles detection, then from positively detected articles additional detection was provided wether the article was about conviction or allegation.

*The aim of this model is not to achieve high accuracy but to present way of 
solving mentioned problem. Accuracy probably will be low due to small amount of articles for training and it's labels.*


Below model ought to predict whether the article is about money laundering activity or not. Then if it is model will predict whether the article is in tone of allegations or convictions.

To make it work I will use 2 models trained on 2 separate datasets.
* 1 dataset is assembled of 25 articles about money laundering and other subjects articles. Thats how model will learn how to distinguish money laundering article from the others. All variables' names belonging to this model start from 'ml' from Money Laundering.
* 2 dataset is assembled of 20 articles with allegations or convictions. Thats how model will learn how to distinguish convictions from allegations. All variables' names belonging to this model start from 'ind' from Indictment.

After creating two separate models I will use them accordingly on the new articles df assembled from articles without labels. Thus, ml_model will be launched on the articles df first to filter out money activity articles only, creating ml_model df. Subsequently ind_model will separate allegations articles and conviction articles from ml_mode df, creating final ind_model df. All can be run through Application.

--------------
------------
## Files descriptions:

* application dataset input - 3 necessery files to run the application
* articles dataset (no labels) - 14 articles to verify in the application
* saved models
      **ml_model - money laundering detection model
      **ind_model - conviction or allegation detection model
* .ipynb - notebook
* train dataset - training articles. Includes 2 sheets 1 for money laundering detection training and 2 for conviction detection training.
