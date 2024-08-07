import java.util.Random;
import java.util.Scanner;

public class GuessTheNumber {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Random random = new Random();

        int rounds = 3; // Number of rounds
        int maxAttempts = 5; // Maximum attempts per round
        int totalScore = 0;

        for (int round = 1; round <= rounds; round++) {
            int numberToGuess = random.nextInt(100) + 1;
            int attempts = 0;
            int score = 0;

            System.out.println("\nRound " + round);

            while (attempts < maxAttempts) {
                System.out.print("Guess a number between 1 and 100: ");
                int guess = scanner.nextInt();
                attempts++;

                if (guess == numberToGuess) {
                    System.out.println("Congratulations! You guessed the number in " + attempts + " attempts.");
                    score = maxAttempts - attempts + 1; // Award points based on attempts
                    break;
                } else if (guess < numberToGuess) {
                    System.out.println("Too low.");
                } else {
                    System.out.println("Too high.");
                }
            }

            if (attempts == maxAttempts) {
                System.out.println("Sorry, you ran out of attempts. The number was: " + numberToGuess);
            }

            totalScore += score;
            System.out.println("Your score for this round: " + score);
        }

        System.out.println("\nTotal score: " + totalScore);
    }
}
