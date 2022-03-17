# Rock_Paper_Scissors_Game
Rock Paper Scissors is a zero sum game that is usually played by two people using their hands and no tools. The idea is to make shapes with an outstretched hand where each shape will have a certain degree of power and will lead to an outcome. This game is played by children and adults and is popular all over the world. 

Steps to Build this Project:
1. Ask the player1 to enter in its move.
2. Check if the player1 entered a valid move.
3. Randomly generate the player2’s move.
4. Use conditionals to figure out if player1 won, lost, or tied.
5. Use a loop to continue asking the player1 for its move.
6. Check if the player1 wants to quit.

Step 1: Ask the player1 to enter in its move.
        Firstly, we import the Scanner class to help us get input from the player1, by adding import java.util.* to the top of our program.
        Then, we create our Scanner variable.
        Next, we print out a message asking the player1 to type in rock, paper, or scissors using System.out.print().
        We store their input in a String called player1Move.

Step 2: Check if the player1 entered a valid move.
        Use a conditional to check whether player1Move is equal to rock, paper, or scissors. If it isn’t equal to rock, paper, or scissors, then we can print out a             message to the player1 stating that its move wasn’t valid!

Step 3: Randomly generate the  player2’s move.
        In order to randomly generate the player2’s move, we can use Math.random(). Math.random() only generates a decimal in between 0 and 1, including 0 and                 excluding 1. But, since there are 3 possible moves in rock, paper, scissors, we need 3 possible random numbers! We can use Math.random() * 3 to generate a             random number in between 0 and 3, including 0 and excluding 3. We can then cast this value to an int so that our random numbers only include 0, 1, and 2 with           no decimals in between.
        Now we need to translate our random number, which can be 0, 1, or 2, into a String player2’s move which is either rock, paper, or scissors.
        For this, we use conditionals to perform the following check: if the random number is 0, then the player2’s move will be rock; if the random number is 1, then         the player2’s move will be paper; if the random number is 2, then the player2’s move will be scissors.

Step 4: Use conditionals to figure out if player1 won, lost, or tied.
        Let’s first check if it was a tie. If the player2’s move was the same as player1's move, then it is a tie.
        We can use .equals() to check equality between two strings. If player1's move is equal to player2’s move, then it is a tie.
        We can now go into an else if and check if the player1 has won. Let’s go through all of the possible situations in which the player1 wins: the player1 has rock         and the player2 has scissors, the player1 has scissors and the player2 has paper, or the player1 has paper and the player2 has rock.
        For this, we can use && and || to make one giant if statement!
        Let’s translate what we just said into code: if (player1's move equals rock and player2's move equals scissors) or (player1's move equals scissors and                 player2's move equals paper) or (player1's move equals paper and player2's move equals rock), then print that the player1 has won. Else, we can print that the         player1 has lost.

Step 5: Use a loop to continue asking the player1 for its move.
        We want to keep asking the player1 to enter its move. For this, we can put all of our code for asking the player1 for its move, checking if player1 entered a           valid move, randomly generating the player2’s move, and figuring out whether the player1 won, tied, or lost in a while(true) loop.
        But now our game will run forever! How do we make the while loop stop?
        In order for a while(true) loop to stop, we need a break statement in the body of the loop. We can ask the player1 if player1 wants to quit the game.

Step 6: Check if the player1 wants to quit.
        In our print statement asking the player1 for its move, we can also ask them to type quit if player1 want to end the game.
        Inside our while loop, let’s use an if statement to check whether or not the player1 entered quit.
        If the player1 did type quit, we can exit out of the while loop using a break statement.

