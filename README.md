_Cheyne Paul DG. Sincioco-2ECEA_PA-3_

_PA#3 PYTHON DATA ANALYSIS (PANDAS)_

# __About the Programming Assignment__
This programming assignment aims to hone our skills in making data frames and series to help analyze large data sets. This task requires us to create variations to data frames and apply them to different problems.

-----------------------------------------------------------------------------------------------------------------------------------------------------
__PROBLEM 1: Save your file as Surname_Pandas-P1.py. Using knowledge obtained from the experiment and demonstrations:__

__a. Load the corresponding .csv file into a data frame named cars using pandas__
__Code__
```
import pandas as pd                #Imports pandas as variable pd
cars = pd.read_csv('cars.csv')     #Reads and loads the file 'cars.csv' into variables 'cars'
```
This code shows the use of loading a __.csv__ file in Python. 

__b. Display the first five and last five rows of the resulting cars__

__Code__
```
h = (cars.head())                        #Gets the first 5 elements in the data frame and stores it to variable h
t = (cars.tail())                        #Gets the last 5 elements in the data frame and stores it to variable t
Combined = pd.concat([h,t], axis=0)      #Concatenates both h and t in a row and stores it to variable combined
display ("b.)", Combined)                #Displays variable combined
```
With the use of __.head()__  function to get the first 5 elements in the data frame, and __.tail()__ function to get the last 5 elements in the data frame, both were combined using __pd.concat([h,t], axis = 0)__, to concatenate the variables in a row to make one table. 

__Code__
```
cars.to_csv('Sincioco_Pandas-P1.py')    #Saves the file as .py
```
The file was saved using __.to_csv()__.

__Example Output:__

<img width="561" height="361" alt="Image" src="https://github.com/user-attachments/assets/179ae44f-64e7-4a57-a36f-e20874fc7bb1" />

-----------------------------------------------------------------------------------------------------------------------------------------------------
__PROBLEM 2: Save your file as Surname_Pandas-P2.py Using the dataframe cars in problem 1, extract the following information using subsetting, slicing and indexing operations.__

__a. Display the first five rows with odd-numbered columns (columns 1, 3, 5, 7...) of cars.__

__Code:__
```
df = cars                                                              
a = df.loc[0:4, ['Model','mpg', 'disp','drat','qsec','am','carb']]#Locates the elements from 0 to 4 and gets its model, mpg, disp, drat, am, and carb
display("a.)", a)                                                 #Displays variable a
```
The code __df.loc[0:4, ['Model','mpg', 'disp','drat','qsec','am','carb']]__ was used to get the elements ranging from 0 to 4, and it specified which parameter to display such as model, mpg, disp, drat, qsec, am, and carb.

__Example Output:__

<img width="384" height="196" alt="Image" src="https://github.com/user-attachments/assets/894375ae-6c7e-4b61-81eb-3f3561f38a03" />

-----------------------------------------------------------------------------------------------------------------------------------------------------
__b. Display the row that contains the ‘Model’ of ‘Mazda RX4’.__

__Code:__
```
b = df.loc[df['Model']=='Mazda RX4']          #Locates the model 'Mazda RX4' and stores it to variable b
display("b.)", b)                             #Displays variable b
```
The code __df.loc[df['Model']=='Mazda RX4']__ was used to locate the model 'Mazda RX4' using equalization symbol. Then, it was displayed.

__Example Output:__

<img width="513" height="90" alt="Image" src="https://github.com/user-attachments/assets/3c3babd0-b6d6-43d6-8306-bff1680005c2" />

-----------------------------------------------------------------------------------------------------------------------------------------------------
__c. How many cylinders (‘cyl’) does the car model ‘Camaro Z28’ have?__

__Code:__
```
c = df.loc[df['Model']=='Camaro Z28',['Model','cyl']]      #Locates the model 'Camaro Z28', gets its model and cyl, and stores it to variable c
display("c.)", c,)                                         #Displays variable c
```
The code __df.loc[df['Model']=='Camaro Z28',['Model','cyl']]__ was used to locate the model 'Camaro Z28', and display its Model and cyl.

__Example Output:__

<img width="147" height="79" alt="Image" src="https://github.com/user-attachments/assets/ebd04025-e11a-4c20-940e-3f1e66fcf1a1" />

-----------------------------------------------------------------------------------------------------------------------------------------------------
__d. Determine how many cylinders (‘cyl’) and what gear type (‘gear’) do the car models ‘Mazda RX4 Wag’, ‘Ford Pantera L’ and ‘Honda Civic’ have.__

__Code:__
```
d = df.loc[[1,18,28], ['Model','gear', 'cyl']]  #Locates the elements 1, 18 and 28, gets its model, gear, and cyl, and stores it to variable d
display("d.)", d)                               #Displays variable d
df.to_csv('Sincioco_Pandas-P2.py')              #Saves the file as .py
```
The code __df.loc[[1,18,28], ['Model','gear', 'cyl']]__ was used to get elements 1,18, and 28, which are Mazda RX4, Honda Civic, and Ford Pantera, and display their Model, gear, and cyl. Also, the file was saved using __.to_csv()__.

__Example Output:__

<img width="216" height="120" alt="Image" src="https://github.com/user-attachments/assets/aed97d99-715f-4217-a0c2-c95ffa72dc42" />

-----------------------------------------------------------------------------------------------------------------------------------------------------
__Lessons Learned:__

This programming assignment taught me to make use of Pandas in various ways. It taught me to load a file and also to save it. To use the locate function to search for something specific in the data frame. This assignment taught me different functions to utilize in different problems.

__Tech(s) Used:__ Jupyter Notebook
