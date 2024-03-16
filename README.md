# Tic-Tac-Toe

## Hosted here -> [TicTacToe](https://prathameshandhare.github.io/Tic-Tac-Toe/)

> [!NOTE]
> * Completely coded using client side scripting, does not require a API, or backend framework.
> * Languages used : HTML as a markup, Javascript (along with JQuery library), and CSS for styling.

> [!WARNING]
> * Refreshing web page will start a new game.

## Supports 2 modes of play:
*  Play against Computer -(one player)
*  Play against friend online -(two player) Both the options implemented using the same HTML, and javascript file, thus decreasing size of total application.
## Features : 

*  Keeps score of player and opponent as well as tie games.
*  Has a Spotify playlist widget on the right panel which is dynamic, i.e changes regularly and the player can choose to listen to music while playing(feature not available on mobile).
*  First move alternates between player and opponent.
*  Player can choose X, O.

# Description of each mode :

## Play against computer (AI):
* Here your opponent is the AI alogorithm which will play against you.
* The algorithm used is the minimax algorithm, optimised with alpha beta pruning.
* Difficulty is auto-adjusted.
  * Adjusted using depth of minimax algorithm.
  * Depth is increased if player wins, thus increasing difficulty.
  * Depth is decreased by 1 if player loses, thus decreases difficulty.
  * Base difficulty starts at 3.
* Alpha beta pruning incorporated - increases the decision making speed of the AI by a huge factor.


## Play against friend:
* Gives you option to create room and join room.
* Both you and your friend can choose the same symbol X or O in your page but response from the other side will always be complimentary.
* MQTT protocol is used for communication.
* Destination name on server is 'prathamesh_tictactoe/' + room  where room is room code.
* MQTT is used because the payload that has to be broadcasted is very small and, its use is very efficient as it doesnt have the overhead of HTTP.
* Person who creates room has to start the game.
