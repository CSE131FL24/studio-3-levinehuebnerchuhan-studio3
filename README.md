package assignment2;
import java.util.ArrayList;
import java.util.Scanner;

public class NimGame {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter the upper limit: ");
        int n = scanner.nextInt();

        ArrayList<Integer> primes = new ArrayList<>(); 

        for (int i = 2; i <= n; i++) {
            boolean isPrime = true;
            for (int j = 2; j * j <= i; j++) {
                if (i % j == 0) {
                    isPrime = false;
                    break;
                }
            }
            if (isPrime) {
                primes.add(i); 
            }
        }
        System.out.println("Prime numbers up to " + n + " are: " + primes);
        scanner.close();
    }
}
