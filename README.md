# TicTacToe

Another TicTacToe implementation in PHP.


## Download

With composer:

``` json
    "alcalyn/tictactoe": "1.0.x",
```


## Usage

``` php
use Alcalyn\TicTacToe\TicTacToe;

$grid = new TicTacToe();

$grid->play(1, 1, TicTacToe::X); // X plays middle
$grid->play(0, 2, TicTacToe::O); // O plays bottom left

// Is left empty ?
$grid->isEmpty(0, 1);

$grid->getCurrentPlayer();
// Returns TicTacToe::X or TicTacToe::O

$grid->getWinner();
// Returns TicTacToe::X, TicTacToe::O, TicTacToe::DRAW or null for no winner.

$grid->getBrochette();
// Returns the 3-in-a-row if there is (or null), with the numbers of the squares:
// Example: [2, 4, 6]
/*
Grid:
0 1 2
3 4 5
6 7 8
*/
```

See the complete [TicTacToe](src/TicTacToe.php) class.

## License

This library is under the [MIT](LICENSE) license.
