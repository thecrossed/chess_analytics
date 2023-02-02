# chess_analytics
To build ELT data pipelines for chess.com players

# Description

[Chess.com](https://www.chess.com/) is a popular online website that chess players play chess for fun or training.

It offers official [API](https://www.npmjs.com/package/chess-web-api) from where developers can fetch data about player profiles, game history and etc.

This project is to fetch chess.com data of chess learners of a local chess club, so that tutors can monitor, understand and make decisions on player performance data.


# Data pipleline
This [diagram](https://docs.google.com/drawings/d/1BzmY8LQ4Q64lc_jIVaKUPrPVy9EqauiTllPp1ptvc1k/edit?usp=sharing) illustrate how does the whole pipeline looks like. For this repo, the work focuses on the ELT steps.

# Schema

### Dimension

Player id - str

Player username - str

Player chess.com - str

### Fact

#### Rating

Player id - str foreign key

Player score - int 

Score type - str

Score update time - timestamp


#### Games

Player id - str foreign key

Game id - str foreign key

Start time - timestamp

End time - timestamp

Game type - str

Is white - boolean

Result - str

Number of moves - int

Start rating white - int

End eating white - int

Start rating black - int

End rating black - int

#### Moves

Game id - str foreign key

Move number - int 

White move - str

Black move - str

