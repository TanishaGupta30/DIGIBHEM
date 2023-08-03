import java.util.Random;
import java.util.*;

public class game {
    public static void main(String[] args){
        int secretNumber, userGuess, attempts = 0;
        int maxAttempts = 10;
        int userScore = 0;
        boolean playAgain = true;

        Random random = new Random();
        Scanner scanner = new Scanner(System.in);

        System.out.println("Welcome to the guessing Game!");

        while(playAgain){
            secretNumber = random.nextInt(100) + 1;

            System.out.println("I have selected a number between 1 and 100.");
            System.out.println("You have " + maxAttempts+ " attempts to guess it.");

            while(attempts < maxAttempts){
                System.out.print("Enter your guess: ");
                userGuess = scanner.nextInt();

                attempts++;

                if(userGuess == secretNumber){
                    System.out.println("Congratulations! You guessed the correct number.");
                    userScore++;
                    break;
                }
                else if(userGuess < secretNumber){
                    System.out.println("To low! Guess higher.");
                }
                else {
                    System.out.println("To high! Guess lower.");
                }

                System.out.println("Attemps remaing: " + (maxAttempts - attempts));
            }
            if(attempts == maxAttempts){
                System.out.println("Sorry, you used up all your attempts.");
                System.out.println("The secret number was: + secretNumber");
            }
            System.out.println("Your score: " + userScore);
            System.out.print("Do you want to play again? (y/n): ");
            String playAgainInput = scanner.next();

            if(!playAgainInput.equalsIgnoreCase("y")){
                playAgain = false;
            }
            attempts = 0;
        }

        System.out.println("Thank you for playing the Guessing Game!!! ");
    }
}

# DIGIBHEM
Project Goal: To create a simple game that is fun to play and that demonstrates the ability to use
Java to create user interfaces, handle input and output, and implement basic game logic.

Project Scope: The project will create a simple text-based game that allows the user to play against
the computer. The game will be a simple guessing game where the user tries to guess a number
between 1 and 100. The computer will randomly generate a number, and the user will have 10
guesses to guess the correct number. The game will keep track of the user score and display it at the
end of the game.

link: https://github.com/TanishaGupta30/DIGIBHEM.github.io

Hope it will help you!!
BEST OF LUCK!!
 
