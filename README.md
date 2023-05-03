Download Link: https://assignmentchef.com/product/solved-cs135-project-6
<br>
<u>Project [6]: Functions</u>

<strong>Project Goals: </strong>

The goals of this project are to:

<ul>

 <li>Get students familiar with the use of functions</li>

 <li>Show students how simple it can be to implement complicated-looking functions.</li>

</ul>




<strong><u>Important Notes:</u></strong>

<ol>

 <li><strong>Formatting: </strong>Make sure that you follow the precise recommendations for the output content and formatting: for example, do not change the text of the problem from “Player 1 enter your selection</li>

</ol>

[row, col]: ” to “Player 1 selection:”. Your assignment will be auto-graded and any change in formatting will result in a loss in the grade.

<ol start="2">

 <li><strong>Comments: </strong>Header comments are required on all files, for each function, and recommended throughout the rest of the program. Points will be deducted if no header/function comments are included.</li>

 <li><strong>Restriction: </strong>The use of goto statements anywhere within this program is prohibited. Points will be deducted if gotois used.</li>

</ol>




<h1>Problem 1</h1>

Write a program that implements the game of Tic-Tac-Toe where you can play against the computer. Player 1 will be the user and player 2 will be the computer. Your program should go through the following steps:

<ol>

 <li>Generate an empty Tic-Tac-Toe board (3×3 array)</li>

 <li>Run a loop until one of the players places three in a row (a player has won) or the table is full (stalemate). This loop should:

  <ol>

   <li>Display the current layout of the table

    <ol>

     <li>Blank spaces are displayed as an underscore</li>

     <li>O for player 1’s moves (user)</li>

    </ol></li>

  </ol></li>

</ol>

<ul>

 <li>X for player 2’s moves (computer)</li>

</ul>

<ol>

 <li>Put spaces between the squares</li>

</ol>

<ol>

 <li>If it is player 1’s turn (the user)

  <ol>

   <li>Ask the user to enter their selection (the location on the board where the O should be placed (row, col))</li>

   <li>Check to make sure that the row and column the user entered is valid</li>

  </ol></li>

</ol>

<ul>

 <li>If the row or column player 1 entered was invalid (outside the bounds of the board or a space that is already occupied) the program should ask the user to enter the option again. If it is player 2’s turn (the computer)</li>

</ul>

<ol>

 <li>Randomly generate a move (row, col) in the board that is not currently occupied (if the computer selects and occupied space generate a new move)</li>

 <li>To generate a random move: generate two random integers, one for the row and one for the column, each between 0 and 2</li>

</ol>

<ul>

 <li>Print out player 2’s move</li>

</ul>

<ol>

 <li>Update the board with player 2’s move</li>

</ol>

<ol start="3">

 <li>If the above loop ends because one of the players has placed three in a row then the program should print out a winning message of that player (see below). Else, it should print out the follow: “Game over, no player wins.”</li>

</ol>




The program should function as follows (items underlined are to be entered by the user):

The current state of the game is:

_ _ _

_ _ _

_ _ _

Player 1 enter your selection [row, col]: <u>1,2</u>

The current state of the game is:

_ O _  _ _ _

_ _ _

Player 2 has entered [row, col]: 1,3 The current state of the game is:

_ O X

_ _ _

_ _ _

Player 1 enter your selection [row, col]: <u>2,2</u>

The current state of the game is:

_ O X

_ O _

_ _ _

Player 2 has entered [row, col]: 2,1 The current state of the game is:

_ O X

X O _

_ _ _

Player 1 enter your selection [row, col]: <u>3,2</u>

The current state of the game is:

_ O X

X O _

_ O _

Congratulations, Player 1 wins!

Your program should implement and use the following functions:

<ul>

 <li>Function name: display_table o Return:

  <ul>

   <li>Nothing oParameters:</li>

   <li>The board as a 3×3 array o Requirements:</li>

   <li>Prints out the following message:</li>

  </ul></li>

 <li>“The current state of the game is:”

  <ul>

   <li>Prints out the current status of the board (as shown above)</li>

  </ul></li>

 <li>Print out an underscore ‘_’ for an empty cell</li>

 <li>Function name: clear_table o Return:

  <ul>

   <li>Nothing</li>

  </ul></li>

</ul>

o    Parameters:

<ul>

 <li>The board as a 3×3 array o Requirements:</li>

 <li>Clear the board for the beginning of the game by making every position in the array an empty cell</li>

 <li>Function name: check_table_full o Return:

  <ul>

   <li>True if the board is full</li>

   <li>False if the board is not full o Parameters:</li>

   <li>The board as a 3×3 array o Requirements:</li>

   <li>Checks to see if the board is full or not</li>

  </ul></li>

 <li>Function name: update_table o Return:

  <ul>

   <li>Nothing oParameters:</li>

   <li>The board as 3×3 array</li>

   <li>The move (row and column)</li>

   <li>The players token (either an X or an O) o Requirements:</li>

   <li>Updates the board with the given player token (either an X or an O) at the given move (row and column)</li>

  </ul></li>

 <li>Function name: check_legal_option o Return:

  <ul>

   <li>True if the given move is legal</li>

   <li>False if the given move is illegal o Parameters:</li>

   <li>The board as a 3×3 array</li>

   <li>The possible move (row and column) o Requirements:</li>

   <li>Checks to see if the given move is within the bounds of the board</li>

   <li>Checks to see if the given move is on an empty cell</li>

  </ul></li>

 <li>Function name: generate_player2_move oReturn:

  <ul>

   <li>Nothing oParameters:</li>

   <li>The board as a 3×3 array</li>

   <li>The move (row and column) o Requirements:</li>

   <li>If the game is not over:</li>

  </ul></li>

 <li>Generate a valid, random move for player 2</li>

 <li>Update the board with the generated move</li>

 <li>Print out the generated move (as seen above)</li>

 <li>Print out the current state of the board</li>

 <li>Function name: check_three_in_a_row o Return:

  <ul>

   <li>Zero if no one has three in a row</li>

   <li>One if player 1 has three in a row</li>

   <li>Two if player 2 has three in a row o Parameters:</li>

   <li>The board as a 3×3 array o Requirements:</li>

   <li>Returns the ID of the player that has three in a row or zero if no one has three in a row</li>

  </ul></li>

 <li>Function name: check_end_of_game o     Return:

  <ul>

   <li>True if the game has ended</li>

   <li>False if the game hasn’t ended o Parameters:</li>

   <li>The board as a 3×3 array o Requirements:</li>

   <li>Returns true or false depending on if the game is over or not</li>

  </ul></li>

 <li>Function name: get_player1_move o Return:

  <ul>

   <li>Nothing oParameters:</li>

   <li>The board as a 3×3 array</li>

   <li>The move (row and column) o Requirements:</li>

   <li>If the game is not over:</li>

  </ul></li>

 <li>Get a possible move from the user (as seen above)</li>

 <li>If the given move is not valid get another move from the user until you have a valid move</li>

 <li>Update the board with the given, valid move</li>

 <li>Print out the current state of the board</li>

 <li>Function name: print_winner o Return:

  <ul>

   <li>Nothing oParameters:</li>

   <li>The board as 3×3 array oRequirements:</li>

   <li>If a player has won prints out the victory message (as seen above) &#x25aa; If the game is a stalemate prints:</li>

  </ul></li>

 <li>“Game over, no player wins.”</li>

</ul>

<strong> </strong>

<strong> </strong>

This is the main function. Copy this into your code and write the ten functions from above in order to make the program work.

int main ()

{

//Declare the tic-tac-toe board    char board[SIZE][SIZE];




//The row and column of the move for either player 1 or 2

int row, col;




//Clear the table    clear_table(board);




//Display the table    display_table(board);

do

{

//Have player 1 enter their move       get_player1_move(board, row, col);




//Generate player 2 move       generate_player2_move(board, row, col);




//Do this while the game hasn’t ended

}while(check_end_of_game(board) == false);




//After the game is over, print who won    print_winner(board);




return 0; }

<strong> </strong>

<strong> </strong>

<strong>Notes: </strong>

<ul>

 <li>You are NOT allowed to use global variables</li>

 <li>You are NOT allowed to change the main function</li>

 <li>You cannot add parameters to any function other than the ones described above SIZE is defined as 3 using a #defineat the top of the program</li>

</ul>




Save your program as tictactoe.c




<strong>Challenge for problem 1 </strong>(10 extra credit points):

Make your program run in a loop. At the end of the game your program should print “Would you like to play again (Y/N): ”. The user will then enter either a ‘Y’ indicating they do want to play again or an ‘N’ indicating they do not want to play again and the program should end. If the user does want to play again the board should be reset and a new game started.

<strong>Note: </strong>

<ul>

 <li>You may change the main function for the challenge</li>

</ul>

Save your challenge separately as tictactoe_c.c


