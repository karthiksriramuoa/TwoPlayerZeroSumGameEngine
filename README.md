# Two-Player, Zero-Sum Game Engine
Simple AI engine written in C# that implements the [alpha–beta pruning algorithm](https://en.wikipedia.org/wiki/Alpha–beta_pruning) to create two-player, [zero-sum](https://en.wikipedia.org/wiki/Zero-sum_game) games like [Tic Tac Toe](https://en.wikipedia.org/wiki/Tic-tac-toe), [Connect 4](https://en.wikipedia.org/wiki/Connect_Four) or [Chess](https://en.wikipedia.org/wiki/Chess).

These three games are all already implemented. Tic-tac-toe and Connect4 are console apps, while chess is a Xamarin Forms + UWP app built with Prism.

## Demo

![Tic-tac-toe & Connect 4 Screenshots](https://raw.githubusercontent.com/ernestoyaquello/TwoPlayerZeroSumGameEngine/master/readme/tic-tac-toe-and-connect-4-screenshots.jpg)

![Chess App Screenshots](https://raw.githubusercontent.com/ernestoyaquello/TwoPlayerZeroSumGameEngine/master/readme/chess-screenshots.jpg)

* In tic-tac-toe, as the algorithm can analyse all the possibilities in the search tree, it is literally impossible to beat the machine.
* In Connect 4, even though the machine is usually good, it is possible to beat it – as the computer cannot study all the possible moves, it has to rely on a score generated by a heuristic function that indicates how likely the player is to win or lose.
* In Chess, experienced players should be able to beat the machine, as the algorithm cannot study all the possible moves, or even just enough of them to create long-term strategies. However, the machine doesn't make silly mistakes, and it is capable of solving simple chess puzzles.

## How to use it
To implement a game, it is necessary to define 3 models:

1. **Move**: Represents a move that a player could make. E.g. "Player 1 puts chip in column 3".
2. **State**: Represents the state of the game board. E.g. in a game like Connect 4, it will contain the information about where each chip is.
3. **Board**: Represents the game board and its mechanics. It has a reference to the *state* and implements and manages its changes, which will be caused by *moves*. This is where the rules and heuristics of the game will be implemented.

For more specific implementation details, the three games that are already in this repository can be used as a reference.

## License
```
Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
