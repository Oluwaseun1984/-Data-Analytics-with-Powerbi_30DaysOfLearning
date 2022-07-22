# -Data-Analytics-with-Powerbi_30DaysOfLearning

![Screenshot (13)](https://user-images.githubusercontent.com/98084177/180437529-23238992-2f5d-4a79-84ca-f89803406af4.png)

Introduction

This is my submission for Microsoft 30 days of learning capstone project Data Analysis using Power Bi.

Project Name: Airlines Delay Storytelling

Problem Objective: 

Story Telling with Power BI. We were asked Create a Report that gives the necessary insights on airline delays, the reasons state the given pattern if any and also provides recommendations to avoid delays by airlines in order to maximize their profits and protect their public image

Data Sourcing

The data was provided by our coach via this links theoyinbooke /30Days-of-Learning-Data-Analysis-Using-Power-BI-for-Students https://raw.githubusercontent.com/theoyinbooke/30Days-of-Learning-Data-Analysis-Using-Power-BI-for-Students/main/Airline%20Project/Airlines.csv

@Theoyinbooke gave credit to kaggle.com @ https://www.kaggle.com/datasets/jimschacko/airlines-dataset-to-predict-a-delay

The data includes just one table with 9 columns: Id, Airline, Flight, Airport From, Airport to, DaysOfweek, Time, Length and Delay

Data Transformation & Modeling

Data Transformation

1

![Screenshot (14)](https://user-images.githubusercontent.com/98084177/180439737-01e4c2ef-9d38-4aa2-b7b0-f0ca7f1cc266.png)

The first step i took was to duplicate the original table into four different tables and renamed them - flight, destination, Date and Delay respectively.

I did this so I would understand the data better and establish a better relationship.

2

![Screenshot (15)](https://user-images.githubusercontent.com/98084177/180440492-2945b058-222d-4194-ad6d-bb9af5d5939e.png)

In the table named flight, I unpivoted other columns excluding ID, airlines and flights then I removed those unpivoted columns..

I changed the data type of the flight column in the flight table to whole numbers.

3

![Screenshot (16)](https://user-images.githubusercontent.com/98084177/180441067-d4d9d6cc-98a3-4be1-8a97-276a4e1977e3.png)

In the table named Destination, I unpivoted other columns leaving behind ID, Airport from and Airport to.

4

![Screenshot (17)](https://user-images.githubusercontent.com/98084177/180441483-2ee9801d-6058-4e6d-b35e-dc6ced7600c8.png)

In the Date table, All other columns were unpivoted then removed aside DaysOfWeek, ID and time Then DaysOFweek column data type was changed to Date.
I duplicated the DaysofWeek column thrice.
The first duplicate was renamed day, then I extracted day by the first name from the column.
The second duplicate was renamed Months, I then extracted month by name from the column.
Finally, the last duplicate was renamed Year and then I extracted Year from the column.

5

![Screenshot (18)](https://user-images.githubusercontent.com/98084177/180442046-d4d30b19-5e76-4678-bec5-708d67d9ca67.png)

In the table named Delay, I unpivoted other columns and then deleted them asides from ID, Time, length and Delay

Then I changed the data type of both length and Delay to whole numbers.

Data Model

![Screenshot (3)](https://user-images.githubusercontent.com/98084177/180442385-7a9218bd-2fe8-4378-bb95-b6f2ab57c8c2.png)

In the modelling section, I used the ID as the key for all tables and then used it to connect all the tables to a fact table which was the airline table.
Findings and Recommendation

![Dashboard](https://user-images.githubusercontent.com/98084177/180442656-4f23c6cf-f5d3-41cf-9b6b-2c72ca96e774.png)

You will notice that despite the fact that OO has more flights travelled compared to WN. Airline OO happens to be the third airline in terms of delay.
What is the cause of this? This is due to the fact that airline WN has a reasonably high distance travelled compared to OO with a corresponding relatively high flight covered.

Meaning that LONGER LENGTH TRAVELLED LEADS TO A HIGHER CHANCE OF DELAY

![Screenshot (5)](https://user-images.githubusercontent.com/98084177/180444129-e841e5c1-0438-49dd-915d-ba97dee80d68.png)

You will notice from this image that Tuesday was the highest day for delays. So I recommend that people should book their flight mostly on weekends to avoid delay.

Recommendation

With this analytics, I would recommend airline WN the airline with the highest delay to reduce their flight covered which is their main reason for a high delay.
From the analytic you would notice that Tuesday and Wednesday had the most delay,  i would advise airlines that they should look at the causes of delay on those two days and avoid them in their subsequent flights.
