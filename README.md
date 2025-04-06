# Chess Game

## Technologies used:

Python with pygame module

## Project Description:

This is a Chess game built using python with pygame module for GUI. It has 2 playing mode either you can play against another human player or against AI. The AI was implemented using Minimax algorithm with alpha beta pruning and with the depth search of 3.

Inorder to model a chessboard within a data structure a 2D array was used with the dimensions of 8x8. The chessboard array could store 64 gametiles objects and each gametile object stored a tile number and a chess piece object.

## Files Description:

1. **Board Directory**:

    - Board.py: In this file we create a class of chessBoard and initialize and declare a 2D array of gametiles with null pieces and then place all the chess pieces on the board on their respective starting positions.
    - move.py: In this file we define some of the special cases in chess for example castling, enpassant rule, check. functions are used to check whether the the player is in check, return moves available in case the player is in check, return moves in case of castling and return moves available in case of enpassant rule.
    - Tile.py: It creates a Tile class which is placed on chessboard array. It can store a position number on the board and a chess piece object.

2. **chess Art directory**: Contains all the images of the chess pieces.

3. **pieces directory**: Contains files in which every chess piece class is defined. Every chess piece class has alliance (indicating whether the piece is white or black) and position ( coordinates on the chessboard ) attributes. It also has legalmove method which is used to calculate the legal moves for that chess piece on the chessboard.

4. **Player directory**:

    - AI.py: Contains the logic for AI algorithm. The AI was implemented using recursive Minimax algorithm with alpha beta pruning and with the depth search of 3. The evaluation function assigned each chess piece a value, White pieces were assigned a positive value based on their rank and black pieces were assigned negative value based on their rank as well. So the total value becomes 0 in the start of the game where each side has all the pieces. The algorithm tried to search all possible moves up to the depth of 3 and calculate which next move could allow it to have best evaluation value.

5. **Playchess.py**: Main file of the program which merges all the functionality from the other files and itself as well to implement all this on pygame GUI.
6. **Screen**:
   Game Screen

## 🧠 Improvements & Reflections

While the current AI performs well in material exchanges and poses a strong challenge to casual players, there is clear room for growth — especially in its **endgame strategy and checkmate execution**.

The AI uses the **Minimax algorithm with alpha-beta pruning**, limited to a depth of 3. This provides quick and reasonably strategic decision-making but can miss deeper tactics, especially in complex positions. Improving the evaluation function to consider board control, piece positioning, and game phase awareness would significantly enhance its effectiveness.

In future versions, I'd like to:

-   Increase search depth using iterative deepening
-   Incorporate **piece-square tables** for smarter evaluation
-   Add **checkmate detection and tactical pattern recognition**
-   Introduce a **difficulty scaler** to adjust AI strength dynamically

Despite its limitations, this project gave me valuable experience in:

-   Building game engines and GUI in `pygame`
-   Structuring modular code across multiple components (board, pieces, AI)
-   Implementing fundamental AI algorithms in a real-time setting

It's a solid foundation for more advanced work in both **AI and game development** — and I'm excited to keep building on it.

## How to Run the Application

`cd chess-game-AI-project`

`pip install -r requirements.txt`

In order to run the game. write the command on terminal or cmd.

`python3 playchess.py`

---

## 🧠 Let’s Connect!

**Tej Jaideep Patel**  
B.S. Computer Engineering  
📍 Penn State University  
✉️ tejpatelce@gmail.com  
📞 814-826-5544

---
