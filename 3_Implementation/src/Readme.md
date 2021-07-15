
Be consistent when naming functions and variables

Decide whether you want to call it a rook or a tower, a bishop or a runner. Prefer using the official names for chess pieces.

You are also not consistent with other things; for example one functions is towerMoves(), another runnerMove() without the s. These functions are also just specializations of getValidMoves(). So be more consistent, and name the first two getValidRookMoves() and getValidBishopMoves().

Add whitespaces to make the structure of your code more clear

Add empty lines between functions, and between major sections within functions. This helps make the structure of your code more clear.

Avoid using system()

Don't call system() for things you can just as well do within C itself. Using system() has a huge overhead, and it is not portable. To clear the screen, you can use ANSI escape codes, which will work in most terminals.
