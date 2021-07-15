Don't use nested functions

Nested functions are a GCC extension, but are not standard C. This means your code is not portable. Just move the functions towerMoves() and runnerMove() outside of getValidMoves(). Of course, now you need to pass x and y as arguments to these functions, and they should return the value of canMove.

Use switch-statements where appropriate

Instead of having a long list of if-statements to check for each possible value of piece in getValidMoves(), write a switch-statement, like so:

switch (piece) 
{

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


