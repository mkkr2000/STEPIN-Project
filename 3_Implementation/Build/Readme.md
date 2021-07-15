  
Use enums to give names to numbers

It would be great if you could write PAWN instead of 1, since it will be much clearer what you are doing in the code. The way to do this is to declare an enum for all possible chess piece types:

enum Type {
    NONE = 0,
    PAWN,
    ROOK,
    BISHOP,
    KNIGHT,
    QUEEN,
    KING,
};
I added NONE as well, it will be useful later to indicate tiles without a piece on them. Once you have done that, instead of if (piece == 1), you can write if (piece == PAWN). Similarly, do this for the color of pieces:

enum Color {
    BLACK = 1,
    WHITE,
};

Define a struct to combine chess piece type and color

Chess piece type and color go together, so it makes sense to make a struct out of this:

struct Piece {
    enum Type type;
    enum Color color;
};

Now we have that, we can combine the arrays board and blackWhite into one:
struct Piece board[8][8];
Now, instead of writing color = blackWhite[y][x], you can write color = board[y][x].color.
Note, you could have made a single enum that listed both the black and white pieces (with names like WHITE_ROOK), and avoid having to create struct Piece, but indeed in your code it makes sense to have piece type and color as separate elements.

Don't use nested functions

Nested functions are a GCC extension, but are not standard C. This means your code is not portable. Just move the functions towerMoves() and runnerMove() outside of getValidMoves(). Of course, now you need to pass x and y as arguments to these functions, and they should return the value of canMove.

Use switch-statements where appropriate
Instead of having a long list of if-statements to check for each possible value of piece in getValidMoves(), write a switch-statement, like so:
switch (piece) {
case PAWN:
    ...
    break;
case ROOK:
    towerMoves();
    break;
case ...:
}
Not only does this improve the structure of your code, the compiler will actually check that you implemented a case-statement for each possible value of piece, and will warn you if you missed one.

Move more code into separate functions
getValidMoves() is a very long function, even with the nested functions moved out of it. It makes sense to also make separate functions for getting the valid moves for each of the other chess piece types. This way, getValidMoves() will be much shorter and clearer to read.

Be consistent when naming functions and variables
Decide whether you want to call it a rook or a tower, a bishop or a runner. Prefer using the official names for chess pieces.

You are also not consistent with other things; for example one functions is towerMoves(), another runnerMove() without the s. These functions are also just specializations of getValidMoves(). So be more consistent, and name the first two getValidRookMoves() and getValidBishopMoves().

Add whitespaces to make the structure of your code more clear
Add empty lines between functions, and between major sections within functions. This helps make the structure of your code more clear.

Avoid using system()
Don't call system() for things you can just as well do within C itself. Using system() has a huge overhead, and it is not portable. To clear the screen, you can use ANSI escape codes, which will work in most terminals. See: https://stackoverflow.com/questions/37774983/clearing-the-screen-by-printing-a-character