# Cookie Cats A/B Testing

## Project Background

This project is adapted from a project on [DataCamp](https://app.datacamp.com/learn/projects/184). However, I used different methods to complete it:

Cookie Cats is a hugely popular mobile puzzle game developed by Tactile Entertainment. It's a classic "connect three" style puzzle game where the player must connect tiles of the same color in order to clear the board and win the level. It also features singing cats. We're not kidding!

As players progress through the game they will encounter gates that force them to wait some time before they can progress or make an in-app purchase. In this project, we will analyze the result of an A/B test where the first gate in Cookie Cats was moved from level 30 to level 40. In particular, we will analyze the impact on player retention.

## Data

The data comes from 90,189 players who installed the game while the A/B test was running. The variables are:

* userid - a unique number that identifies each player.
* version - whether the player was put in the control group (gate_30 - a gate at level 30) or the group with the moved gate (gate_40 - a gate at level 40).
* sum_gamerounds - the number of game rounds played by the player during the first 14 days after install.
* retention_1 - whether the player came back and played one day after installing.
* retention_7 - whether the player came back and played seven days after installing.

When a player installed the game, he or she was randomly assigned to either gate_30 or gate_40.

## A/B Test and Results

I performed permutation tests to determine whether the percent difference in retention rates between the gate_30 and gate_40 groups was nonzero, for both one-day and seven day retention rates. While the data showed that the one-day retention rate for the gate_30 group was 1.34% higher than the one-day retention rate for the gate_40 group, this difference was not statistically significant at the 5% level (p = 0.06). However, the seven-day retention rate for the gate_30 group was 4.5% higher than the seven-day retention rate for the gate_40 group, and this result was statistically significant (p = 0.0). So, there is strong evidence that the seven-day retention rate is higher when the first gate is placed at level 30 instead of level 40. One possible reason for this is hedonic adaptation--placing the first gate earlier in the game keeps players from playing too much and getting bored, thus prolonging their enjoyment of the game. As a follow-up to this project, it would be useful to test whether placing the first gate even earlier (e.g., at level 20 or 25) increases retention even more.
