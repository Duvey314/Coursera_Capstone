# Coursera_Capstone
Github repo for the data science professional capstone course.
* [The Problem](#the-problem)
* [The Data](#the-data)

### The Problem

Car accidents happen every day all over the world. Due to the energy involved in these collisions, there is a high chance that someone is seriously injured in one of these accidents. To properly treat these victims, medical personnel need to be ready to administer aid immediately. Having an estimation of the severity of the collision can help first responders prepare treatment and potentially save lives. This project is meant to help serve first responders so that they can have an estimation of the severity of the accident before arriving on the scene to know what type of aid is needed.


### The Data

The [dataset](https://www.seattle.gov/Documents/Departments/SDOT/GIS/Collisions_OD.pdf) contains real collision data from the Seattle Police Department (SPD) all the way back to 2004. It contains information on the severity of the collision which is what we will be trying to predict. There are over 35 other columns to use to help us predict the severity. Some columns are simply ID columns that will not be useful for this project. Others contain a plethora of information but need to be analyzed further like the collision code dictionary which has 85 different collision types like 'Vehicle Backing Hits Pedestrian' or 'Vehicle Hits Other Road or Construction Machinery'. More analysis will be needed to find the best columns to use to train our model. Once the columns have been selected, the dataset will be split into multiple train and test sets from which a classification model can be developed.
