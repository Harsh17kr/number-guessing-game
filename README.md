
import java.util.Scanner;

public class Nggnew {

    public static void guessingNumber() {
        // Scanner Class
        Scanner sc = new Scanner(System.in);

        // Generate the numbers
        int number = 1 + (int) (100 * Math.random());
        int n = 10;
        int i, guess;
        System.out.println("A number is chosen between 1 to 100. Guess the number" + " within 10 trials.");
        for (i = 1; i < n; i++) {

            System.out.println("Guess the number:");

            // Take input for guessing
            guess = sc.nextInt();

            // If the number is guessed
            if (number == guess) {
                System.out.println("Congratulations!" + " You guessed the number.");
                break;
            } else if (number > guess && i != n - 1) {
                System.out.println("The number is " + "greater than " + guess);
            } else if (number < guess && i != n - 1) {
                System.out.println("The number is" + " less than " + guess);

            }
        }
        if (i == n) {
            System.out.println("You have exhausted" + " K trials.");
            System.out.println("The number was " + number);
        }
    }

    public static void main(String arg[]) {
        guessingNumber();
    }
}
