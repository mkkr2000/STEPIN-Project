  
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

