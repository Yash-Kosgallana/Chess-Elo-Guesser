# Chess-Elo-Guesser
Data analysis of close to 30,000 chess games and model development to predict average elo of chess players given pgn.

Started by using simple features such as blunders per game_lenth (eg per move). Used stockfish to evaluate the rating of each position and hence understand various features such as the average eval change per move and the variance in the eval. Eg, eval change per move should be lower in higher rated oppponents udue to making more "best moves". Added more features later on such as number of major piece moves in the first ten moves, wheter bishop pair was maintained, number of legal moves etc. For example, the position tends to get "locked" in higher rated games leading to a lower number of possible legal moves.

The task was seperated into two methods, one to determine the average elo of a player based on a game, eg both black and white get different ratings and a combined average. 
Running various models, gave the mean absolute error to be only several points below the average difference, meaning a person guessing would have a similar idea to that of the model. This is due to the difficulty in predicting the rating of an indivuidal based off of one game. It is also important to note that the second method is whats done even by experts, as experts often use an opponents elo to determine a players as a game may have been submitted due to exceptional performance, as seen from Gotham Chess's Guess the Elo series.

Attempting to solve the first method, the feature of player color existed. Running stat models regression analysis gave the coeficient of player colour to be approximately five, meaning black has a 5 elo point disadvantage. Eg, if two players are 1200, black is more like 1195 and white is 1200.

The second method seemed to be more useful in that a person would underpreform against the model. This is as the final model was able to predict to 220 elo points the average rating.
