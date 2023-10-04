# Using Kmeans to find new NBA PlayerTypes
Inspired by a few Medium articles, in this repository we'll group NBA players using Kmeans algorithm to analyse each type of players offensive and to suggest new signings.

In the world of professional basketball, particularly the NBA, players exhibit diverse playing styles and strengths offensively. This project aims to apply K-Means clustering to group NBA players based on their possession percentages in various play-types in 2019 & 2020 seasons. By doing so, we seek to uncover distinctive player profiles, enhance performance analysis in the NBA.
Additionally, we aim to propose potential player acquisitions to replace those with similar playing styles, contributing to strategic decision-making for teams.

## The data

In this project we use differents datasets. For the data of possesion percentatges in various play-types, we use 2 datasets, one for the 2018-2019 season and the other one for de 2019-2020 season. The 2019-2020 season dataset is in Kaggle and the 2018-2019 we find it in a Github repostiory mentioned in the end of this article. 

To analyse each new player-type and to suggets potential player acquisitions to teams, we use data extracted from Basketball Reference (https://www.basketball-reference.com/).

## Clustering
First of all, we read the data and clean it so that we can work comfortable. Our dataframe has 583 players with 11 variables. Apart from the name and the team of the players and the season, we have the frequency of each play-style. These play-styles are: 
- Isolation
- Pick & Roll Ball Handler
- Pick & Roll Roll Man
- Transition
- Post up
- Spot up
- Cut
- Handoff
  
Once we have the data cleaned, we can start to build our Kmeans model. 
We decide to use Kmeans but it's very important to choose wisely how many clusters to model. So our first step is to use the elbow method to find the optimal number of clusters in our data. Here is the result:

![Alt text](img/elbow_method.png)

Analysing the graph, we would declare that the optimal k is 4. However, we know nowadays there aren't only 4 types of offensive players, so we declare k=6.

Now, we fit the model with k=6 and add the new clusters to our data.

## Results

After reviewing how the model grouped our data, we can define the 6 different offensive player-type and see their characteristics in this HeatMap:

![Alt text](<img/HeatMap Clusters.png>)
