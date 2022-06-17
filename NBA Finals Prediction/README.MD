
# Predicting result of NBA finals games 
![](https://staticg.sportskeeda.com/editor/2022/06/407f8-16554441902885-1920.jpg)
"All we do is shoot 3's and win championships"

These were the words uttered by Klay Thompson after winning his *4th* NBA championship in collaboration with Stephen Curry after defeating the Celtics in Game 6 of the NBA Finals. It's no secret that they've revolutionized the way basketball is played through their 3 pointers. In fact, the league wide 3-point rate has increased by 77% in the last decade. But exactly how crucial is the 3-pointer to a teams success? And has history shown for other statistical categories to be more important.

## Project Intro/Objective
The purpose of this project is to use NBA Finals data from 1980-2017 to view the most influential statistics toward a teams win. 

### Methods Used
* Data Visualization
* Data Cleaning
* Stepwise Regression
* Binomial Regression

### Technologies
* Python
* VSCode
* Pandas
* Jupyter
* Excel


## Project Description and Variables
The data was taken from Kaggle and lists the box score from each game of the finals from 1980-2017. Below are the variables in the dataset. It also shows whether or not the team won the championship. Our response variable will be "Win".
- Year: The year the series was played
- Team: The name of the team.
- Win: 1 = Win. 0 = Loss
- Home: 1 = Home team. 0 = Away team.
- Game: Game #
- MP - Total minutes played. Equals 240 (48x5=240) if game did not go to overtime. MP>240 if game went to overtime.
- FG - Field goals made
- FGA - Field goal attempts
- FGP - Field Goal Percentage
- TP - 3 Point Field Goals Made
- TPA - Three point attempts
- TPP - three point percentage
- FT - Free throws made
- FTA - Free throws attempted
- FTP - Free throw percentage
- ORB - Offensive rebounds
- DRB - Defensive rebounds
- TRB - Total rebounds
- AST - Assists
- STL - Steals
- BLK - Blocks
- TOV - Turnovers
- PF - Personal fouls
- PTS - points scored

### Data Cleaning
- Null values removed from both files
- Columns being numeric was confirmed
- Checked for outliers
- Added a column "champs" for whether or not the team won the championship (1=yes, 0=no)
- Merged the data so that the data was in one csv file


### EDA
During my exploratory data analysis, I created graphs using variables that I thought were most likely to influence a teams win chance. These variables include points, assists, rebounds, turnovers, and a few more. Below are highlights from the visualizations.

![](C:/Users/omerc/desktop/4.png)
![](/desktop/5.png)
![](desktop/3.png)
![](/desktop/2.png)
![](desktop/1.png)

### Model Building
I determined the best model using backward stepwise regression. Starting with a full model, I removed variables until the remaining variables were significant. The photo below shows the model I began with and my final model. We
![](desktop/6.png)
![](/desktop/7.png)

## Model Prediction
I then used the box score from a game not in the dataset with my model. I'm sure you can guess which.
![](https://fivethirtyeight.com/features/the-warriors-latest-title-might-be-their-most-surprising/)
With the way Golden State played in Game 6 of the 2022 finals, they had a 1.893 log odds of winning the game. This results in a probability of 0.654 according to my model. 
![](desktop/8.png)

## Conclusion
As it turns out, the 3 pointer is just as crucial as we thought. Although the reason the Dubs were able to win their fourth title, it is not the most *mathematically significant* stat. We find that having more steals, less turnovers, and total rebounds are more important. To no surpise, these are all *possession* statistics. Keeping the ball safe and taking it away from the other team is the best offense. The more you have the ball, the more chances you have to score.

## Resources
* [Dataset](https://www.kaggle.com/datasets/daverosenman/nba-finals-team-stats)
* [Template for README](https://github.com/sfbrigade/data-science-wg/blob/master/dswg_project_resources/Project-README-template.md)
