# CODSOFT_Task1

Project Summary: This is the task of  the Titanic dataset to build a model that predicts whether a passenger on the Titanic survived or not. This is a classic beginner project with readily available data. The dataset typically used for this project contains information about individual passengers, such as their age, gender, ticket class, fare, cabin, and whether or not they survived.

Steps Followed:

    Data Cleaning: Remove all errors, inconsistencies and duplicates data from data sheet.
    Data Processing: Prepared the data for analysis by organizing and formatting it appropriately.
    Data Analysis: Employed various analytical techniques to derive insights and draw meaningful conclusions.
    Data Visualization: Presented the findings in a visually appealing manner through charts and graphs.
    Reports: Compiled a comprehensive Dashboard to  summarizing the analysis and its outcomes.
    

Key Question of the dashboard :

    What is the Total Passenger ?
    Out of Total Passenger, how many Total Survived and Total Dead ?
    What is the Average Age of Passenger ?
    In which Class more Percentage of Passenger Survived & Dead ?
    How many Passengers were Survived and No-survived in Percentages ?
    How many Total Passenger by Age Group of Young, Middle and Old Age resp ?


Insight of the dashboard :

417 is the Total Passenger were in Titanic.
Total Passenger Survived  152 and No Survived 265.
The Averege Age of Passenger is 23.98
In First Class more Percentage of Passenger Survived of 47% & In Second Class more Percentage of Passenger Dead of 68%
Total Percentage of Passenger Survived 36.45% and Total Percentage of Passenger Not-survived 63.55%
By Age group Total Passenger of Young Age127, Middle Age 277 and Old Age 13.


DAX Query :

    Total Passenger = COUNT(Data[PassengerId])
    Total Survived = CALCULATE(COUNT(Data[Survival]), Data[Survival] = "Survive")
    Total Dead = CALCULATE(COUNT(Data[Survival]), Data[Survival] = "No Survive")
    Boarding Location = DISTINCTCOUNT(Data[Embarked])
    Total Fare = SUM(Data[Fare])
    Average Age = AVERAGE(Data[Age])
    Age Group = IF(Data[Age]<18, "Young Age", If(Data[Age]<60, "Middle Age", "Old Age"))
    Boarding Types = IF(Data[Embarked] = "C", "Cherbourg", IF(Data[Embarked] = "S", "Southampton", "Queenstown"))
    Passenger Class = IF(Data[Pclass] = 1, "First Class", IF(Data[Pclass] = 2, "Second Class", "Third Class"))








