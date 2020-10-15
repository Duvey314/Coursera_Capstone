# Coursera_Capstone
Github repo for the data science professional capstone course.
### Table of Contents

- [The Problem](#the-problem)
- [The Data](#the-data)
- [Methodology](#methodology)
- [Results](#results)
- [Discussion](#discussion)
- [Conclusion](#conclusion)

# The Problem

With the growth of the suburbs in the last 50 years, more people have to drive to work every day. This has led to an increase in traffic and [pedestrian fatalities](https://www.ghsa.org/resources/news-releases/pedestrians20). This project applies machine learning to accidents involving pedestrians and predicts severity of injury to aid medics responding to the accident. 


# The Data

The [dataset](https://www.seattle.gov/Documents/Departments/SDOT/GIS/Collisions_OD.pdf) contains real collision data from the Seattle Police Department (SPD) all the way back to 2004. It contains information on the severity of the collision which is what we will be trying to predict. For this project, we will be looking at the following columns to assess pedestrian injury severity.

* SEVERITYCODE - The severity of the accident. This is our y variable and the value we are trying to predict. A 0 means that there was property damage only and a 1 means that there was some physical injury.
* ST_COLCODE - The code of the collision. Used to describe the accident.
* PEDCOUNT - Whether or not there were pedestrians involved.
* PERROWNOTGRNT - Whether or not the pedestrians right of way was granted.
* SPEEDING - Was the driver speeding?

There are a number of data manipulations that had to be performed on the data to transform it into the correct format for the machine learning model. The first was to convert the values in speeding and pedestrian right of way to binary values so that they could be analyzed by our model.

The second piece was to drop our na values and empty values in the state collision code. These values cannot be used in our model.

After this we binned our pedestrian values into a binary value since there was a large disparity between the number of accidents with pedestrians and without. 

Lastly, we had to change the datatype of our collision codes from an object to an integer value.

# Methodology

To get a better understand of how each variable effects the final we can create some simple visualizations.


![Pedestrian Accidents](https://github.com/Duvey314/Coursera_Capstone/blob/master/Images/accidents_with_pedestrians.PNG)

We can see that there was more likely to be some physical injury when a pedestrian is involved in an accident. This make sense since the pedestrian does not have a seatbelt or airbag to protect them during a crash.

![Speeding Accidents](https://github.com/Duvey314/Coursera_Capstone/blob/master/Images/accidents_while_speeding.PNG)

Contrary to what I would have expected, it looks like speeding doesn't have as much of an impact on accident severity.

![Pedestrian RoW](https://github.com/Duvey314/Coursera_Capstone/blob/master/Images/accidents_given_row.PNG)

At first this chart seems backwards but when you look at the columns, you can see that a 1 means that the pedestrian right of way was NOT granted. This means that accidents were more severe when the car did not respect the pedestrian right of way which is what we would expect

I

# Results

| Algorithm               | **Jaccard**    | **f1-score**  | **Precision** | **Recall**  |
| :---                    |     :---:      |     :---:     | :---:         | :---:       |
| **Logistic Regression** | 0.73           | 0.85          |    0.78       | 0.75        |
| **Random Forest**       | 0.75           | 0.85          |   0.78        | 0.74        |

# Discussion

For this problem we are worried about the Recall value of our model because we are more worried about predicting the injury to people.

Both the Logistic Regression model and the Random Forest model are accurate predictors of injury. However, our logistic regression model had a slightly higher recall value and is likely a better choice for the model.

# Conclusion

The model works well for this data set but there are a number of factors to consider for future research. The first is looking at other types of classifiers like neural nets or KNN. This might improve results but likely not drastically. I think the biggest improvement would come from a change in the dataset. There is a class imbalance in the data and addressing this imbalance could make the model more accurate.

In addition, the accident severity is limited to a binary value. If there was data that had more detail about the severity of the accident, we could provide better predictions for accident severity for pedestrians instead of property.
