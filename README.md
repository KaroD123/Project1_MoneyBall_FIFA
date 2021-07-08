# Project1_MoneyBall_FIFA

## Objectiv
Performing an end-to-end analysis putting into practice what I have learned so far. Get a model to predict the value of a player.

### Subquestions:
1. Order players by Overall Rating (OVA).
2. Which country has in average the best players (by OVA)?
3. Are the best 10 players by OVA more or less agressive than the average?
4. Where are most of the players from?

## Dataset 
In this project, I used the provided [**fifa21_male2.csv**](https://github.com/Ironhack-Data-0621-Remote/Project_FIFA_MoneyBall/tree/main/Data) dataset.

[Here](https://www.kaggle.com/ekrembayar/fifa-21-complete-player-dataset?select=fifa21_male2.csv) details about the dataset can be found here as well. 

This data set includes:

1. **EA Sports FIFA 19 Game** data:

    |   |   |
    |---|---|
    |  Player Name | Club of the Player   |
    | League  | Position  |
    | Pace  |  Shooting |
    |  Passing | Dribbling  |
    | Defending|Physical|
    |||


1. **Transfermarkt** extra info by player:

    |   |   |
    |---|---|
    |  Date of Birth| Nationality   |
    | Height  | Foot  |
    | Day Joined the current club  |  Day of Contract End |
    |  Market Value of the Player |  |
    |||


2. **Instagram and Facebook** data by player:

   - Number of followers on Instagram
   - Number of likes on Facebook of the club in which the player has a contract

4. **ESPN FC** data from the past 5 years performance of each player

   - **GS:** Games Started
   - **SB:** Games Substituted
   - **G:** Goals Scored
   - **A:** Assists
   - **SH:** Shots
   - **SG:** Shots on Goal
   - **FC:** Fouls Committed
   - **FS:** Fouls Suffered
   - **YC:** Yellow Cards
   - **RC:** Red Cards

## Workflow
First, I answerd my suquestions and than started to clean the data. In this process I droped some unnessecary columns for some different reasons. For example, I did't needed the names and pictures/logos for my regression model or some data wad shared multiple times in the dataframe.
After some general cleaning the data, I check the correlation of some caolumns and droped some that were unnessecary. After applying a boxcox transformation, I checked the p-values and droped some more columns which had an high p-value. Furthermore, I removed the outliers for all the columns.

To get the best result I compared the boxcox transformation to a normalization. The boxcox was best with an R2 of 0.9551 after removing columns with an high p-value

