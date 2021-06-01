# Tic-Tac-Toe
2 Player GUI based Tic-Tac-Toe Game 
![tictacopening](https://user-images.githubusercontent.com/79473081/120360756-bbb05080-c326-11eb-8953-c8d5a7e55b4d.png)


Tic Tac Toe is one of the most played games and is the best time killer game that you can play anywhere with just a pen and paper. If you don’t know how to play this game don’t worry let us first understand that.

The game is played by two individuals. First, we draw a board with a 3×3 square grid. The first player chooses ‘X’ and draws it on any of the square grid, then it’s the chance of the second player to draw ‘O’ on the available spaces. Like this, the players draw ‘X’ and ‘O’ alternatively on the empty spaces until a player succeeds in drawing 3 consecutive marks either in the horizontal, vertical or diagonal way. Then the player wins the game otherwise the game draws when all spots are filled.


The interesting Python project will be build using the pygame library. Pygame is a great library that will allow us to create the window and draw images and shapes on the window. This way we will capture mouse coordinates and identify the block where we need to mark ‘X’ or ‘O’. Then we will check if the user wins the game or not.

-------Steps to Build a Python Tic Tac Toe Game--------

First, let’s check the steps to build Tic Tac Toe program in Python:

Create the display window for our game.
Draw the grid on the canvas where we will play Tic Tac Toe.
Draw the status bar below the canvas to show which player’s turn is it and who wins the game.
When someone wins the game or the game is a draw then we reset the game.
We need to run our game inside an infinite loop. It will continuously look for events and when a user presses the mouse button on the grid we will first get the X and Y coordinates of the mouse. Then we will check which square the user has clicked. Then we will draw the appropriate ‘X’ or ‘O’ image on the canvas. So that is basically what we will do in this Python project.

![X](https://user-images.githubusercontent.com/79473081/120362389-a3413580-c328-11eb-9f94-6636ba3cb1cc.png)
![O](https://user-images.githubusercontent.com/79473081/120362397-a6d4bc80-c328-11eb-922b-18017e2de92a.png)

1. Initializing game components
So let’s start by importing the pygame library and the time library because we will use the time.sleep() method to pause game at certain positions. Then we initialize all the global variables that we will use in our Tic Tac Toe game.

2. Initializing Pygame window
We use the pygame to create a new window where we’ll play our Tic Tac Toe game. So we initialize the pygame with pg.init() method and the window display is set with a width of 400 and a height of 500. We have reserved 100-pixel space for displaying the status of the game.

The pg.display.set_mode() initializes the display and we reference it with the screen variable. This screen variable will be used whenever we want to draw something on the display.

The pg.display.set_caption method is used to set a name that will appear at the top of the display window.

3. Load and transform images
The Python project uses many images like the opening image that will display when the game starts or resets. The X and O images that we will draw when the user clicks on the grid. We load all the images and resize them so that they will fit easily in our window.

4. Define the functions
Now we create a function that will start the game. We will also use this function when we want to restart the game. In pygame, the blit() function is used on the surface to draw an image on top of another image.

So we draw the opening image and after drawing, we always need to update the display with pg.display.update(). When the opening image is drawn, we wait for 1 second using time.sleep(1) and fill the screen with white colour.

Next, we draw 2 vertical and horizontal lines on the white background to make the 3×3 grid. In the end, we call the draw_status() function

The draw_status() function draws a black rectangle where we update the status of the game showing which player’s turn is it and whether the game ends or draws.

The check_win() function checks the Tic Tac Toe board to see all the marks of ‘X’ and ‘O’. It calculates whether a player has won the game or not. They can either win when the player has marked 3 consecutive marks in a row, column or diagonally. This function is called every time when we draw a mark ‘X’ or ‘O’ on the board.

The drawXO(row, col) function takes the row and column where the mouse is clicked and then it draws the ‘X’ or ‘O’ mark. We calculate the x and y coordinates of the starting point from where we’ll draw the png image of the mark.

The userClick() function is triggered every time the user presses the mouse button.

When the user clicks the mouse, we first take the x and y coordinates of where the mouse is clicked on the display window and then if that place is not occupied we draw the ‘XO’ on the canvas. We also check if the player wins or not after drawing ‘XO’ on the board.

5. Run the tic tac toe game

To start the game, we will call the game_opening() function. Then, we run an infinite loop and continuously check for any event made by the user. If the user presses mouse button, the MOUSEBUTTONDOWN event will be captured and then we will trigger the userClick() function. Then if the user wins or the game draws, we reset the game by calling reset_game() function. We update the display in each iteration and we have set the frames per second to 30.


---------------Summary------------------

With this project in Python, we have successfully made the Tic Tac Toe game. We used the popular pygame library for rendering graphics on a display window. We learned how to capture events from the keyboard or mouse and trigger a function when the mouse button is pressed. This way we can calculate mouse position, draw X or O on the display and check if the player wins the game or not. I hope you enjoyed building the game.
