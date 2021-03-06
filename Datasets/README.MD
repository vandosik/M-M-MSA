# Dataset info
## [Challenger_Ranked_Games.csv](https://www.kaggle.com/gyejr95/league-of-legends-challenger-ranked-games2020?select=Challenger_Ranked_Games.csv)
> This is the main dataset we use in [Labs](https://github.com/vandosik/M-M-MSA/tree/master) [1](https://github.com/vandosik/M-M-MSA/tree/master/Lab_1), [2](https://github.com/vandosik/M-M-MSA/tree/master/Lab_2) and [3](https://github.com/vandosik/M-M-MSA/tree/master/Lab_3)

### Introduction

This Dataset has Challenger Ranked 26000 Games,
Data include Blue team and Red team information


### Contents

League of Legends is MMORPG game where two teams (red and blue) fight to win. 
Each team has five independent players and the task of the game is to destroy the main building of the enemies.
This data contains key information that can affect the win or loss in the game.
League of Legends includes objects, champions, and minions.
Objects here represent dragons, barons, messengers, towers, suppressors, and more.
The heart of the data is the result of the match between the blue and red teams.
Therefore, the factor analysis that affects the win or loss of the game and the methodology to predict the win or loss of the game will be the most important points in analyzing the data.
In our work we analyse <ins> the blue team stats only</ins>.


### Additional data description

* ward : Map lighting tools
* gold : Money to buy items
* tower : Attack turrets protecting our camp or enemy camp
* inhibitors : You can summon our team's superminions(very very powerful) by breaking the suppressor.
* dragon, baron : Objects that can receive buffs when destroyed
* Minion : Small summoners from each team who can earn gold by killing
* Level : champion level (min : LV 1 / max : LV 18)

## [timeStamped_Challenger_Ranked_Games.csv](https://github.com/vandosik/M-M-MSA/blob/master/Datasets/timeStamped_Challenger_Ranked_Games.csv)
> This dataset was used in [Lab 4](https://github.com/vandosik/M-M-MSA/tree/master/Lab_4)

### Introduction

For [Lab 4](https://github.com/vandosik/M-M-MSA/tree/master/Lab_4) it was necessary to have timestamps. The original dataset does not contain them, so the data was retrieved using the Riot.API.

### Source

The raw data from which the dataset was formed was extracted using [Riot.API](https://developer.riotgames.com/apis). We used a full dataset with [raw data for all game matches for 2020](https://www.kaggle.com/gyejr95/league-of-legendslol-ranked-games-2020-ver1).

### What we have done

We [merged](https://github.com/vandosik/M-M-MSA/blob/master/Datasets/Timestamps_parser.ipynb) the timestamps from full DS with our main DS by gameID column. Data we have got has Unix-TS format, so we converted it to Python 3 timestamps format and have got [new csv file](https://github.com/vandosik/M-M-MSA/blob/master/Datasets/timeStamped_Challenger_Ranked_Games.csv).