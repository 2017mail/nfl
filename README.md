# nfl
Goal: A play recommender for nfl teams based on past performance of players on their teams.

Choose any two NFL teams, and any game status (score, time left, ball position, down status), and

Dataset source:
https://www.kaggle.com/maxhorowitz/nflplaybyplay2015

Method:
Use Monte Carlo to simulate games and decide who to give the ball to on each play.  

Simplifications: 
For the sake of time, the following assumptions have been made in this model.

1. Every play takes 20 seconds.
2. No kickoffs/punts.  Teams attempt to make a play on 4th down and turn it over at the spot if the play fails.
3. Only passing and rushing are allowed.  
4. Only touchdowns are implemented (no field goals, no 1-point or 2-point conversions).
5. No defense data is implemented.
6. No anomalous plays are taken into account (turnovers, etc).


Todo:
(Cosmetic)
Remove any of the simplifications of the game.

(ml/ai)
1. Incorporate the time plays take into MC model.

2. Incorporate data from defense somehow. Rerun MC with the additio of artificial parameters on the effectiveness of defense; i.e. the defending team can choose to defend against a rushing or a passing play, with different outcome distributions depending on the choices the offensive team made.
Due to lack of data (i.e. defensive formation, offensive formation, which players are in any given play), this is probably the simplest solution.

3. Add fatigue factor for rushing; possibly for passing, for the receivers.  I.e. check if rushers are less effective after consecutive plays and take this into account in the MC simulations.
