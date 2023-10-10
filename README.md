## Tetris Game
This project contains a Java-based implementation of the classic Tetris game. Tetris is an addictive game where different shapes need to be placed and lines need to be cleared to prevent stacking.

### How to Run

1. Clone the project to your development environment or computer.
2. Run the main class `Tetris.java`.
3. A "Tetris" window will open to start the game. You can control the game using the arrow keys on your keyboard.

### Game Controls

- **Left Arrow Key**: Move the shape to the left.
- **Right Arrow Key**: Move the shape to the right.
- **Up Arrow Key**: Rotate the shape clockwise.
- **Down Arrow Key**: Accelerate the shape's downward movement.
- **Space Key**: Drop the shape instantly.
- **P Key**: Pause or resume the game.

### Game Rules

- The game continues until any unplaced shape reaches the top of the screen.
- Completed lines on the screen are automatically cleared, and the player's score increases.
- An unplaced shape can be moved or rotated as long as it does not collide with the shapes above.
- The objective of the game is to achieve the highest score, which is based on the number of cleared lines.

## Code Review

### `Board.java`

The `Board` class represents the Tetris game board and contains the core logic of the game. Some key features of this class are:

- The `initBoard(Tetris parent)` method initializes the game board and allows it to focus on the main window.
- The `start()` method initiates the game and starts the game loop.
- The `pause()` method pauses or resumes the game.
- The `paintComponent(Graphics g)` method is responsible for rendering the board and tetrominoes.
- The `doDrawing(Graphics g)` method contains the logic for drawing the board and tetrominoes.
- The `dropDown()` and `oneLineDown()` methods allow the tetromino to move down or move one line down.
- The `clearBoard()` method clears the game board.
- The `pieceDropped()` method is called when a tetromino lands and places it on the board.
- The `newPiece()` method creates a new tetromino and positions it at the top of the game board.
- The `tryMove()` method handles collision detection when attempting to move a tetromino.
- The `removeFullLines()` method clears completed lines and updates the score.
- The `drawSquare()` method is responsible for drawing a square.

### `Shape.java`

The `Shape` class represents Tetris tetrominoes. Some key features of this class are:

- An enum named `Tetrominoe` nested inside, which represents different tetromino shapes.
- The `initShape()` method initializes tetromino properties and coordinates.
- The `setShape()` method sets the shape of the tetromino.
- The `setRandomShape()` method randomly selects a tetromino shape.
- The `rotateLeft()` and `rotateRight()` methods perform the rotation of the tetromino.

### `Tetris.java`

The `Tetris` class creates the main window for the game. Some key features of this class are:

- The `initUI()` method initializes the main window and the game board.
- The `main()` method serves as the entry point for the game and starts the game.
