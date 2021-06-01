# FINAL-ASSIGNMENT-IV-
https://github.com/Abbeytec/FINAL-ASSIGNMENT-IV-/
package ABIODUN21910091;

import java.util.HashSet;
import java.util.Scanner;
import java.util.Set;

public class PrimeNumber {
    private static int num;

    public static void main(String[] args) {

        Scanner inputNumber = new Scanner(System.in);
        System.out.println("Enter a positive whole number: ");
        num = inputNumber.nextInt();

        boolean flag = false;
       for (int i = 2; i < Math.sqrt(num); i++) {

            // condition for non prime number
            if (num % i == 0) {
                flag = true;
                break;
            }
        }

        if (!flag) {
            System.out.println(num + " is a prime number and factors are: " + num);
        } else {
            System.out.println(num + " is a composite number and factors are:");

            //Create a HashSet to store factors
            Set<Object> primeFactors = new HashSet<>();

            for (int i = 2; i <= num; i++) {
                if (num % i == 0) {
                    primeFactors.add(i); // prime factor
                }
            }
            for (Object factor : primeFactors) {
                System.out.print(factor + ", ");
            }

            System.out.println();
        }

        getIteration(num);
    }

    // Calculate the number of iterations
    private static void getIteration(int num) {
        int count = 1;
        while (count < num - 1) {
            count++;
        }
        System.out.println("With 1st method number of iteration is: " + count);
    }
}
