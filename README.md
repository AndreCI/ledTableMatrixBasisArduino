# ledTableMatrixBasisArduino

This repo is a template to program stuff to be displayed on my 32x32 LED Matrix table, and controller by my 4 SNES controllers, in C++.

How to use it:
 - 
 - Keep the "setup" function as it is. It will run once, at the start of the code, and set hardware stuff up.
 - The "loop" function is an infinite loop, running the code. Use it as a "main", and call functions or anything else in it.
 - Keep the "checkAllButtons()" at the start of the loop. It will gather all player inputs, and fill the playerButtonPushed[NUMBER_PLAYERS][12] with the it. It is filled as follows, with 0/1 for each button: UP - RIGHT - DOWN - LEFT - START - SELECT - A - B - X - Y - L - R. Hence, playerButtonPushed[0][1] means player 0 has pushed button RIGHT.
 - Fill the 32x32 global variable "LEDMatrix" as you wish, with "Black", "White", "Blue", "Red", "Green" and "Purple", which are global colour variables (it's actually simply 0-5 numbers)
 - At the end of the loop, keep the "clearLEDMatrix()", and then outputDisplay(), which will take your "LEDMatrix" and plot it on the table through a mapping.
 
 If needed, you can also use digitalOutputDisplay() to plot the LEDMatrix in the Arduino "Moniteur Série".
