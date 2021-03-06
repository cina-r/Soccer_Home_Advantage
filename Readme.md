# Soccer Home Advantage

## Goal
Due to the COVID-19 pandemic, the football/soccer season 2020/21 was very special since (nearly) all professional matches were played in **empty stadiums**. For football enthusiasts like me, this is a real bummer. However, it offers the **unique opportunity** to statistically study the influence of fans on the team performance.


## Setup

### Setting up the virtual environment

1. >pip install virtualenv
2. >python -m venv env
3. > cd .\env\Scripts
4. >activate
5. >pip install -r requirements.txt
6. >python -m ipykernel install --name=\<choose-a-name-to-be-displayed-in-jupyter\>

### Working with the data
All relevant steps of my analysis are available in the **home_advantage.ipynb** Notebook.


## Data
### Data Description
In order to have a significant amount of data, I've collected fixtures and results from Europe's top 5 leagues (according to the [official UEFA ranking](https://www.uefa.com/memberassociations/uefarankings/country/#/yr/2021)) in the seasons 2018/19 and 2020/21. Season 18/19 is the last one that ended before the start of the pandemic and is therefore chosen to represent a &#8216;regular&#8217; season, whereas season 20/21 lies completely in the pandemic and (almost) all matches are played without spectators.   
Note that I've excluded the last two matchdays of the English Premier League from the analysis because, at this stage, (a limited amount of) fans were allowed to enter the stadium again.  

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
In the image above, you can see the percentage of all matches that were won by the **home** team, plotted for Europe's top 5 leagues in the mentioned seasons. Averaging over all five leagues yields a home win ratio of 44.8%  in the pre-covid season 18/19 and 40.8% in the covid-season 20/21. Hence, the chance of winning a home game increases by 4.0% when there are spectators in the stadium. 

### Away Win Ration
![Away Team Victories [%]](plots//europe_away_win_percentages.png)   
The second image shows the same plot as the first one but with **away** instead of home team win percentage. Equivalently, we see a lower average value in season 18/19 with 29.6% than in 20/21 with 34.2%. The chance of winning an away game decreases by 4.6% with spectators in the stadium. Note that home and away team ratios are not perfectly correlated since in league football a draw is also a possible match result. 

### Table Position 
The English Premier League (EPL) shows the highest discrepancy between the seasons' average home win ratios with a diffence of 11%. Let's take a deeper look into the EPL!  
![Home Team Victories of top, mediocre and bottom teams in EPL [%]](plots//epl_top_medi_bottom.png)   
I've split the teams within each season into top (1-7), mediocre (7-13) and bottom (14-20) teams and investigated the home win ratios seperately for each of those three groups. As you can clearly see, the effect is much higher for the top teams than for the mediocre and bottom teams. It seems like success goes hand in hand with having a vibrant fan support in the own stadium.   
  
    
**General remark**:  
Correlation doesn't necessarily imply causality - the results are partly my personal interpretation. 
