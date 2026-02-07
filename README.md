# Soccer Home Advantage

## Goal
The COVID-19 pandemic made the 2020/21 football season unlike any other, with nearly all professional matches played behind closed doors. For fans, this was a huge letdown. But it also created a unique natural experiment: a chance to analyze statistically how crowd support affects team performance.

## Setup

### Setting up the virtual environment

1. `pip install uv`
2. `uv sync`

### Working with the data
All relevant steps of my analysis are available in the **home_advantage.ipynb** Notebook.


## Data
### Data Description
To ensure a sufficiently large dataset, I collected fixtures and results from Europe’s top five leagues (according to the [official UEFA ranking](https://www.uefa.com/memberassociations/uefarankings/country/#/yr/2021)) for the 2018/19 and 2020/21 seasons. The 2018/19 season was the last to conclude before the pandemic and is therefore used as a proxy for a “regular” season. In contrast, the 2020/21 season took place entirely during the pandemic, with (almost) all matches played behind closed doors.

Note that the final two matchdays of the English Premier League were excluded from the analysis, as a limited number of spectators were allowed back into stadiums at that stage.

### Data Source
#### Season 2018/19  
* https://fixturedownload.com/results/bundesliga-2018  
* https://fixturedownload.com/results/serie-a-2018  
* https://fixturedownload.com/results/la-liga-2018  
* https://fixturedownload.com/results/epl-2018  
* https://fixturedownload.com/results/ligue-1-2018  
#### Season 2020/21  
* https://fixturedownload.com/results/bundesliga-2020  
* https://fixturedownload.com/results/serie-a-2020  
* https://fixturedownload.com/results/la-liga-2020  
* https://fixturedownload.com/results/epl-2020  
* https://fixturedownload.com/results/ligue-1-2020  


## Results
### Home Win Ratio
![Home Team Victories [%]](plots//europe_home_win_percentages.png)  
The figure above shows the percentage of matches won by the **home** team across Europe’s top five leagues in the seasons considered. When averaging over all five leagues, the home-win rate is 44.8% in the pre-COVID 2018/19 season and 40.8% in the COVID-affected 2020/21 season. This corresponds to a 4.0 percentage point higher probability of winning a home match when spectators are present in the stadium.

### Away Win Ration
![Away Team Victories [%]](plots//europe_away_win_percentages.png)   
The second figure shows the same analysis, but for **away** wins instead of home wins. Consistently, the average away-win rate is lower in the 2018/19 season (29.6%) than in 2020/21 (34.2%). In other words, the probability of winning an away match decreases by 4.6 percentage points when spectators are present in the stadium. Note that home- and away-win rates are not perfectly complementary, since a draw is also a possible outcome in league football. 

### Table Position 
Among the five leagues, the English Premier League (EPL) shows the largest gap in average home-win rates between the two seasons – an 11 percentage point difference. This makes the EPL a particularly interesting case study, so let’s take a closer look.    
![Home Team Victories of top, mediocre and bottom teams in EPL [%]](plots//epl_top_medi_bottom.png)   
I divided the teams in each season into three groups – top (1–7), mediocre (8–13) and bottom (14–20) – and analyzed the home-win rates for each group separately. As the figure shows, the effect is much stronger for top teams than for mediocre or bottom teams. This suggests that on-field success is closely associated with strong home support and a vibrant atmosphere in the stadium.
    
**General remark**:  
Of course, correlation does not imply causation, and these results should be interpreted with appropriate caution. The conclusions drawn here are, to some extent, based on my own interpretation.