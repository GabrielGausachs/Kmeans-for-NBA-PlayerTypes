# Using Kmeans to find new NBA PlayerTypes
Inspired by a few Medium articles, in this repository we'll group NBA players using Kmeans algorithm to analyse each type of players and to suggest new signings.

In the world of professional basketball, particularly the NBA, players exhibit diverse playing styles and strengths. This project aims to apply K-Means clustering to group NBA players based on their possession percentages in various play-types in 2019 & 2020 seasons. By doing so, we seek to uncover distinctive player profiles, enhance performance analysis in the NBA.
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
- Handoff.
Once we have the data cleaned, we start to define how we are going to group this players.
