Cheyne Paul DG. Sincioco-2ECEA_PA-3

PA#3 PYTHON DATA ANALYSIS (PANDAS)

# __About the Programming Assignment__
This programming assignment aims to hone our skills in making data frames and series to help analyze large data sets. This task requires us to create variations to data frames and apply them to different problems.
------------------------------------------------------------------------------------------------------------------------------------------------------
__PROBLEM 1: Save your file as Surname_Pandas-P1.py. Using knowledge obtained from the experiment and demonstrations:__

__a. Load the corresponding .csv file into a data frame named cars using pandas__

__b. Display the first five and last five rows of the resulting cars__

__Code__
```
import pandas as pd 
cars = pd.read_csv('cars.csv')
display ("a.)", cars)
h = (cars.head())
t = (cars.tail())
Combined = pd.concat([h,t], axis=0)
display ("b.)", Combined)
cars.to_csv('Sincioco_Pandas-P1.py')
```
__Description:__ This problem shows the use of loading a __.csv__ file in Python. With the use of __.head()__  function to get the first 5 elements in the data frame, and __.tail()__ function to get the last 5 elements in the data frame, both were combined using __pd.concat()__, to concatenate the functions to make one table. Also, the file was saved using __.to_csv()__.

__Example:__

```
Output:
'b.)'
Model	mpg	cyl	disp	hp	drat	wt	qsec	vs	am	gear	carb
0	Mazda RX4	21.0	6	160.0	110	3.90	2.620	16.46	0	1	4	4
1	Mazda RX4 Wag	21.0	6	160.0	110	3.90	2.875	17.02	0	1	4	4
2	Datsun 710	22.8	4	108.0	93	3.85	2.320	18.61	1	1	4	1
3	Hornet 4 Drive	21.4	6	258.0	110	3.08	3.215	19.44	1	0	3	1
4	Hornet Sportabout	18.7	8	360.0	175	3.15	3.440	17.02	0	0	3	2
27	Lotus Europa	30.4	4	95.1	113	3.77	1.513	16.90	1	1	5	2
28	Ford Pantera L	15.8	8	351.0	264	4.22	3.170	14.50	0	1	5	4
29	Ferrari Dino	19.7	6	145.0	175	3.62	2.770	15.50	0	1	5	6
30	Maserati Bora	15.0	8	301.0	335	3.54	3.570	14.60	0	1	5	8
31	Volvo 142E	21.4	4	121.0	109	4.11	2.780	18.60	1	1	4	2
```
------------------------------------------------------------------------------------------------------------------------------------------------------
__PROBLEM 2: Save your file as Surname_Pandas-P2.py Using the dataframe cars in problem 1, extract the following information using subsetting, slicing and indexing operations.__

__a. Display the first five rows with odd-numbered columns (columns 1, 3, 5, 7...) of cars.__

__b. Display the row that contains the ‘Model’ of ‘Mazda RX4’.__

__c. How many cylinders (‘cyl’) does the car model ‘Camaro Z28’ have?__

__d. Determine how many cylinders (‘cyl’) and what gear type (‘gear’) do the car models ‘Mazda RX4 Wag’, ‘Ford Pantera L’ and ‘Honda Civic’ have.__

__Code:__
```
df = cars
a = df.loc[0:4, ['Model','mpg', 'disp','drat','qsec','am','carb']]
b = df.loc[df['Model']=='Mazda RX4']
c = df.loc[df['Model']=='Camaro Z28',['Model','cyl']]
d = df.loc[[1,18,28], ['Model','gear', 'cyl']]
display("a.)", a,"b.)", b,"c.)", c,"d.)", d)
df.to_csv('Sincioco_Pandas-P2.py')
```

__Description:__ This problem shows the use of the locate function in a data frame. With the use of the locate function to locate certain elements and parameters in a data frame, __df.loc[0:4, ['Model','mpg', 'disp','drat','qsec','am','carb']]__ was used to get the elements ranging from 0 to 4, and it specified which parameter to display. __df.loc[df['Model']=='Mazda RX4']__ was used to locate Mazda RX4 using equalization symbol. __df.loc[df['Model']=='Camaro Z28',['Model','cyl']]__ was used to locate Camaro Z28, and display Model and cyl. __df.loc[[1,18,28], ['Model','gear', 'cyl']]__ was used to get elements 1,18, and 28, which are Mazda RX4, Honda Civic, and Ford Pantera, and display their Model, gear, and cyl. Also, the file was saved using __.to_csv()__.

__Example:__
```
Output:
'a.)'
Model	mpg	disp	drat	qsec	am	carb
0	Mazda RX4	21.0	160.0	3.90	16.46	1	4
1	Mazda RX4 Wag	21.0	160.0	3.90	17.02	1	4
2	Datsun 710	22.8	108.0	3.85	18.61	1	1
3	Hornet 4 Drive	21.4	258.0	3.08	19.44	0	1
4	Hornet Sportabout	18.7	360.0	3.15	17.02	0	2
'b.)'
Model	mpg	cyl	disp	hp	drat	wt	qsec	vs	am	gear	carb
0	Mazda RX4	21.0	6	160.0	110	3.9	2.62	16.46	0	1	4	4
'c.)'
Model	cyl
23	Camaro Z28	8
'd.)'
Model	gear	cyl
1	Mazda RX4 Wag	4	6
18	Honda Civic	4	4
28	Ford Pantera L	5	8
```
------------------------------------------------------------------------------------------------------------------------------------------------------
__Lessons Learned:__

This programming assignment taught me to make use of Pandas in various ways. It taught me to load a file and also to save it. To use the locate function to search for something specific in the data frame. This assignment taught me different functions to utilize in different problems.

__Tech(s) Used:__ Jupyter Notebook
