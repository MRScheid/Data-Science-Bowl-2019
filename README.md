# Data-Science-Bowl-2019
'Data Science Bowl 2019 Project.ipynb'- Code for cleaning, munging, EDA, model building and evaluation for the Kaggle Data Science Bowl 2019.  

Using gameplay data from a children’s educational app, 'Measure Up', the goal of the competition was to use this data to predict child's performance on assessments within the app.  Using factors of gameplay that I found influenced assessment performance, I built a kNN model that had 83% accuracy in predicting the child’s performance on assessments.  

More info on the competition can be found here: 
https://www.kaggle.com/c/data-science-bowl-2019/overview

The data for this competition can be found here:
https://www.kaggle.com/c/data-science-bowl-2019/data


Next steps / future directions (with more time):
- Parse the '0' accuracy group to see if there are subgroups in there that can be dropped due to lack of activity
- Improving the features used to predict the child's assessment performance
    - Look at the # of help events the child initiated (more help events may mean higher performance)
    - Look at the responses on games -- performance on games may predict assessment performance.
    - Look at exploration of toys in 'Activity' type gameplay.  Higher toy exploration may predict later performance
- Improve prediction model:
    - Test other classification models
    - Tune hyperparameters
    - Try boosting and / or stacking models to improve performance. 
    
    


