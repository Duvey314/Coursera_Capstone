# Coursera_Capstone
Github repo for the data science professional capstone course.
- [Coursera_Capstone](#coursera_capstone)
    - [The Problem](#the-problem)
    - [The Data](#the-data)
    - [Methodology](#methodology)
    - [Results](#results)
    - [Discussion](#discussion)
    - [Conclusion](#conclusion)

### The Problem

With the growth of the suburbs in the last 50 years, more people have to drive to work everyday. This has lead to an increase in traffic and [pedestrian fatalities](https://www.ghsa.org/resources/news-releases/pedestrians20). This project applies machine learning to accidents involving pedestrians and predicts severity of injury to aid medics responding to the accident. 


### The Data

The [dataset](https://www.seattle.gov/Documents/Departments/SDOT/GIS/Collisions_OD.pdf) contains real collision data from the Seattle Police Department (SPD) all the way back to 2004. It contains information on the severity of the collision which is what we will be trying to predict. For this oroject, we will be looking at the following columns to assess pedestrian injury severity.

* SEVERITYCODE - The severity of the accident. This is our y variable and the value we are trying to predict. A 0 means that there was property damage only and a 1 means that there was some physical injury.
* ST_COLCODE - The code of the collision. Used to describe the accident.
* PEDCOUNT - Whether or not there were pedestrians involved.
* PERROWNOTGRNT - Whether or not the pedestrians right of way was granted.
* SPEEDING - Was the driver speeding?

There are a number of data manipulations that had to be performed on the data to transform it into the correct format for the machine learning model. The first was to convert the values in speeding and pedestrian right of way to binary values so that they could be analyzed by our model.

The second piece was to drop our na values and empty values in the state collision code. These values cannot be used in our model.

After this we binned our pedestrian values into a binary value since there was a large disparity between the number of accidents with pedestrians and without. 

Lastly we had to change the datatype of our collision codes from an object to an integer value.

### Methodology



### Results

| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |

### Discussion

### Conclusion
