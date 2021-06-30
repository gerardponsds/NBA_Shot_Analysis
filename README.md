# NBA: 3-POINT SHOT TREND

In this repository we are going to look through some NBA shot data from the seasons 1997-1998 to 2019-2020, in order to get some insights and statisics about the impact 3-point shots have in the game. The data has been provided by **data.world** and can be found [here](https://data.world/sportsvizsunday/june-2020-nba-shots-1997-2019). The goal is to explore the data on the shots an look at how they evolved through the years, and also look at some interstings statisctics.

### DATA CLEANING

Luckily for us, this dataset does not have missing values, so we won't have to deal with them. However, we will work with a selection of the attributes, we will transform some of them and also we will get rid of some datapoints based on some assumptions: 

* An imporant attribute we will like to work with is the **season**, but it is not present in the given dataset. However, it is contained in the *Game ID*, so we will transform that column in order to facilitat further manipulation.
* Additionally, we would like to work with shots made by the player in standard conditions, so we will remove shots made from the **own side of the court**, as those are made as a last resource in the last seconds of a period or game.

## ANALYSIS

It is commonly believed that every time, more and more players and teams focus on 3-point shots rather than 2-point ones, as some of the most valuable and well known NBA players have a high 3-point accuracy. We will start by proving that assumption by visualizing a headmap of shot attempts in different seasons, to observe if there is a pattern:

<p align="center">
  <img src="/images/shotlocation.png"  alt="drawing" width="700"/>
</p>


It can be easily seen that every time more and more scoring attempts are from **over the three point line**, and some shot positions that once where important (i.e. lateral shots or mid-range at 45º) have now lost importance. These 3-point shots are the ones more visually appealing and the ones that the fans chear the most, but let's look now at some data that can point out towards why this shift is happening.

We will start by looking the **average point per shot** over the seasons, to know if it really pays off to throw more 3-point shots:


<p align="center">
  <img src="/images/pointspershot.png"  alt="drawing" width="450"/>
</p>

As this last metric suggests, it is **more efficient to attempt a 3-point shot**, hence it is not strage that more players and team focus on them. However, it must be noted that the 2-point shot efficiency is on the increase. This increase is directly related to the **accuracy of the shots**, and the fact that the 3-point shots' efficiency has remained stable during the past decades indicates that its accuracy has also remained fairly constant. Let's see that:

<p align="center">
  <img src="/images/2vs3pointsaccuracy.png"  alt="drawing" width="450"/>
</p>

As expected, the data reflects our **previous conclusions**. The increase in accuracy could be to multiple factors, including players being more selective when chosing to attempt 2 point shots or defenders not paying a lot of attention to this kind of shots, among others. Let's see now the **actual impact** that 3-pointers have in a game by observing three metrics: 

#### EVOLUTION OF SHOT ATTEMPTS

In order to quantify the data presented in the first heatmap figure, we will explore the percentage of shot attempts between 2-point and 3-point shots : 

<p align="center">
  <img src="/images/2VS3pointersattemppercentage.png"  alt="drawing" width="450"/>
</p>

We can clearly see that number of three pointers attempts with respect to the 2-point shots has **more than doubled** over the last decades, but we should explore what does it really mean. More 3-point shots are attempted but 2-point shot attempts remain the same? Less 2-point shots are thrown? There has been a different increase/decrease rate in both? Has the total number of shots per game changed?

#### SHOT ATTEMPTS PER GAME

To answer these questions, we should look at the average shot attempts per game: 

<p align="center">
  <img src="/images/shotattemptsperday.png"  alt="drawing" width="450"/>
</p>

The figure speaks for itself. The total number of shots has increased due to a **significant increase of 3-point shots attempts**, a value that has been increasing in a higher rate nearly each season, whereas the number of 2-point shots has been decreasing.

#### EVOLUTION OF FIELD POINTS

This last conclusions and results should also be seen when exploring the field points per game, and their origins:


<p align="center">
  <img src="/images/fieldpointpergame.png"  alt="drawing" width="450"/>
</p>

As seen previouly, the accuracy had increased (2-point shots) or remained stable (3-point shots), so combined with the fact that there where more shot attempts per game, we easily observe the expected result: **more field points are scored per game**. Also, we can observe the expected growing contribution of 3-point shots.

### CONCLUSIONS

We have showed the increasing trend in throwing 3-point shots and the impact it has on games. Interestingly, we have also seen an increase in the accuracy of 2-point shots, that if it keeps increasing, could lead to an stop to the 3-point shot trend.


## APPENDIX

As the dataset contained a lot of additional data, some additinal metrics and statistics have been computed:

#### PLAYERS WITH MORE 3-POINTS IN A GAME

<p align="center">
  <img src="/images/average3pointspergame.png.png"  alt="drawing" width="450"/>
</p>

#### PLAYERS WITH THE HIGHER 3-POINTS/GAME RATE

<p align="center">
  <img src="/images/playerswithmore3points.png"  alt="drawing" width="450"/>
</p>

#### 3-POINT ACCURACY DEPENDING ON LOCATION

<p align="center">
  <img src="/images/zonedependent3points.png"  alt="drawing" width="450"/>
</p>
