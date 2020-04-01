# Data-Science-Bowl-2019
'Data Science Bowl 2019 Project.ipynb'- Code for cleaning, munging, EDA, model building and evaluation for the Kaggle Data Science Bowl 2019.  

Using gameplay data from a children’s educational app, 'Measure Up', the goal of the competition was to use this data to predict child's performance on assessments within the app.  Using factors of gameplay that I found influenced assessment performance, I built a kNN model that had 83% accuracy in predicting the child’s performance on assessments.  

More info on the competition can be found here: 
https://www.kaggle.com/c/data-science-bowl-2019/overview

The data for this competition can be found here:
https://www.kaggle.com/c/data-science-bowl-2019/data

## File Organization and Function 

- Data Science Bowl 2019.ipynb - Notebook for running the data input, processing, visualization and model creation, fitting and testing on the Data Science Bowl 2019 dataset.    

## Environment and Instructions
- In 'Data Science Bowl 2019.ipynb' point to the directory where the data is downloaded.  This should be on line 1 of the second code cell. 

## Features
- The 3 features of gameplay used were time spent in different types of gameplay, specifically:
    - Clip
    - Game
    - Activity

## kNN justification and considerations

I chose to use a kNN model here because kNN is pretty simple and intuitive as a first pass for a small number of input features (only 3).  I also knew the number of clusters that I was looking for -- there were only 4 classes of assessment performance and this is the only hyperparameter to tune for a kNN.  Since kNN is a non-parametric algorithm, it was a safe choice since it doesn't require the features I engineered to meet any assumptions. 

One potential drawback of using the kNN on this dataset is the slight imbalance in the number of examples for each 'accuracy_group' in the training data.  Certain groups are overrepresented and this can cause a bias towards these groups, causing those groups that are underrepresented to be misclassified.  

Another drawback of using the kNN is the sensitivity to outliers.  In the game_time data there are outliers in the '0' group, that spent a lot of time in the game, but never took assessments.  This can affect the accuracy of the classification.  

## Next steps / future directions (with more time):
- Parse the '0' accuracy group to see if there are subgroups in there that can be dropped due to lack of activity
- Improving the features used to predict the child's assessment performance
    - Look at the # of help events the child initiated (more help events may mean higher performance)
    - Look at the responses on games -- performance on games may predict assessment performance.
    - Look at exploration of toys in 'Activity' type gameplay.  Higher toy exploration may predict later performance
- Improve prediction model:
    - Test other classification models
    - Tune hyperparameters
    - Try boosting and / or stacking models to improve performance. 
    
    


