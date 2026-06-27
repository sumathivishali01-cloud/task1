# task1
package com.internship.greeting;

import java.util.Scanner;

public class PersonalizedGreeting {

    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);

        try {
            System.out.print("Enter your name: ");
            String name = scanner.nextLine();

            System.out.print("Enter your age: ");
            int age = scanner.nextInt();

            int yearsTo100 = 100 - age;

            System.out.println("\n----- Personalized Greeting -----");
            System.out.printf("Hello %s! You are %d years old.%n", name, age);

            if (yearsTo100 > 0) {
                System.out.printf("You have %d years until you turn 100.%n", yearsTo100);
            } else if (yearsTo100 == 0) {
                System.out.println("Congratulations! You are 100 years old.");
            } else {
                System.out.printf("You turned 100 %d years ago.%n", Math.abs(yearsTo100));
            }

        } catch (Exception e) {
            System.out.println("Invalid input! Please enter a valid age.");
        } finally {
            scanner.close();
        }
    }
}
