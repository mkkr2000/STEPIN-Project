
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

D
