# GuessNo-
import java.util.Random;
import java.util.Scanner;

public class NumGuess {
    public static void main(String[] args) {
        Random rand = new Random();
        int numberToGuess = rand.nextInt(100) + 1;
        Scanner scanner = new Scanner(System.in);
        int guess;

        System.out.println("Welcome to the number guessing game!");
        System.out.println("Guess a number between 1 and 100:");

        while (true) {
            guess = scanner.nextInt();

            if (guess == numberToGuess) {
                System.out.println(" oho...!! Congratulations , you guessed the number & you won the game!");
                break;
            } else if (guess < numberToGuess) {
                System.out.println(" Oops...! You Guess very small number.please Try again:");
            } else {
                System.out.println(" Oops...! You Guess very big number.please Try again:");
            }
        }

        scanner.close();
    }
}
