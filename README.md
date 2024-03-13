import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int reversed = 0;

        while (n > 0) {
            reversed = reversed * 10 + n % 10;
            n = n / 10;
        }

        if (isPrime(reversed)) {
            System.out.println("Twisted prime number");
        } else {
            System.out.println("Not a twisted prime number");
        }

        System.out.println(reversed);
    }


    public static boolean isPrime(int num) {
        if (num < 2) {
            return false;
        }
        for (int i = 2; i <= Math.sqrt(num); i++) {
            if (num % i == 0) {
                return false;
            }
        }
        return true;
    }
}

