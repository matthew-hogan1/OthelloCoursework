# OthelloCoursework
Othello coursework code,readme and .doc

<H1> AI Algorithm </H1>


The algorithm for the ai to determin is made up of primarily 2 functions. The first of which is called ai move 

<H2>ai_move</H2>
![ai_move](https://github.com/user-attachments/assets/37624769-1e51-4f3f-8be5-d87dc894ac9e)

The function takes in one argument which is the number of moves left. First a list called potential_moves is created and this will be used to store all the moves that the ai could make on its turn aswell as the strengtth of each move. Then the program attempts to iterate through every cell in the board. This is done by a nested for loop as the board is a 2d array of rows and columns. If an exception is hit then the exception is logged and the move (-1,-1) is returned. This is impossible to get from the board as tthe indeces of the list cant be negative so therefore the move function knows the ai cant make a move and it can handle it appropriately. If an exception is not hit it checks if it would be a legal move for the ai to place a light counter on that square by calling the function legal_move. If it is a legal move a copy of the board is created. The reason a copy of the board is created is because the ai simulates the moevs it could make for the next 3 turns, and we dont want to alter the actual game board whilst trying out moves. Then the counter is placed at the coordinates on the copy board, and the counters that need to be flipped are got using the function get_cells_to_convert. Then the function flips all the cells that need to be flipped and gets the number of counters that have been flipped to light as a result of the move. This serves like a score for the move as the more flips the better the move. After that, the ai simulates the next 2 turns which would be the next player and ai turn using simulate_placement. This simulates both players playing 1 optimal move each and returns the overall number of light counters gained. This is done so the ai can pick a better move for tthe long term game rather than justt the current move. This score is then added to the number of counters flipped by making the move and the co-ordinates of the move and its score are added to the potential_moves list. Once all the cells have been evaluated, the program chooses the best move by selecting the move with tthe highest score and returns the co-ordinates of the move. 


  




