# StellarClassification

**Task:** Build and train a Machine Learning Algorithm to classify celestial objects based on EM Spectrum emissions and Red Shift.

**Purpose:** Enable professional and armature scientists to automate and reduce error of classification of celestial object observations.


**The code:** Using Colaboratory and written in the python language, this project is broken down into six sections, each serving an important function in analysis of the data and meeting the objectives of this project.
1.	Establishment of Tools and Importing the Data
2.	Data Cleaning
3.	Data Visualization 
>  a.	Exploratory Visualization
>>    i.	Extract critical information
>  b.	Explanatory Visualization
>>    i.	Generate presentation ready graphics
4.	Preprocessing the data
>  a.	Ensures the data is ready for analysis and modeling
5.	Modeling and Evaluation
>  a.	K-Nearest Neighbor (sklearn)
>  b.	Random Forest Regression Model (sklearn)
>  c.	Gradient Boosting Model (sklearn)

**Findings:** Based on model perfromance, the Gradient Boosting Classifier (tuned hyperparameters: max_depth = 5, max_leaf_nodes = 30, n_estimators = 100) achieved the best results with the greatest potential to improve as new data is introduced. Below is a breakdown of data used and discarded to make the most efficent model and best model performance:
-	Target Data
>  o	'class'
>>  o	Star
>>  
>>  o	Galaxy
>>  
>>  o	Quasar 
>>  
-	Critical Data to modeling
>  o	'u'
>  
>  o	'g'
>  
>  o	'r'
>  
>  o	'i'
>  
>  o	'z'
>  
>  o	'redshift'  
>  
-	Data Discared as irrelivant to analysis:
>  o	 'obj_ID'
>  
>  o	 'alpha'
>  
>  o	 'delta'
>  
>  o	 'run_ID'
>  
>  o	 'rerun_ID'
>  
>  o	 'cam_col'
>  
>  o	 'field_ID'
>  
>  o	 'spec_obj_ID'
>  
>  o	 'plate'
>  
>  o	 'MJD'
>  
>  o	 'fiber_ID'
>  
- Best model performance:
![GBM performance](https://user-images.githubusercontent.com/94806791/155918077-9c529f2b-0028-4d7a-ac99-2867d6ec8a7b.png)

I choose this model with the above hyperparameters because it achieved the highest accuracy, f1, recall, and percision scores for all classes. It score was actually equal to the performance of both the RandomForest default and unted models, however tunning the GBM model yeilded a more significant imporvement in score and therefore while likely continue to get imporve relative to the Random Forest as additional data and be feed back into the model. While GBM model classified stars perfectly, it is important to note that the model had some trouble differentiating between galaxies and quasars. Quasars have the highest instances of both false positives and false negatives (with false negatives being the worse performance - recall score of 0.92).

This model would be an excellent aid to professional and amature scientists for streamlining the classification of celestial objects. Individuals can utilize this model with confidence that approximately 98% of the time it will be accuracte. However, because this model has some challange with differentiating between galaxies and quasars, it may require the occasional use of traditional / analog classification means to confirm model predictions. Overtime, with additional data, this model can continue to be refined to reduce error.

**Visual Representation of the Dataset and Relationship between RedShift, EM Emission, and Class:**
![Redshift and Emissions](https://user-images.githubusercontent.com/94806791/155918290-14572c72-79c9-4186-ba71-1143a0fd700d.png)
> Scatter plot shows general distinction between all three classes when comparing ultraviolet light emitted and the redshift of each celestial object. Given the similarities between plots of each EM Emission and the redshift, I am using the ultraviolet emission as embliatic of all the EM emissions to demonstrat the relasionship between redshift, em emission and class.

**Recommendation:**
1. Immediately roll out model for use by professional and amateur astronomers

> Caveat: classification should be verified through traditional methods

2. Incorporate existing data from other observation systems to improve model


3. Continue to collect data from both professional and amateur astronomers to improve model




Techincal Presentation: https://drive.google.com/file/d/17S1tuzFvFo9HGHj1VHbx2K9JIMfS6LN8/view?usp=sharing
