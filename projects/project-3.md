---
layout: project
type: project
image: images/ics.jpeg
title: Cotton
permalink: projects/ics
# All dates must be YYYY-MM-DD format!
date: 2018-04-28
labels:
  - Java
summary: An ICS-211 Program that fulfills most of the basics of programming.
---
An online course I took that consists the basics of Java.

Code Overview:
```java
import java.io.FileWriter;
import java.io.IOException;
import java.io.Writer;
import java.util.Scanner;
import java.util.concurrent.ThreadLocalRandom;

public class javaBasics {

    public static void main(String[] args) {
        int a[] = new int[20];
        for (int i = 0; i < 20; i++) {
            a[i] = ThreadLocalRandom.current().nextInt(1, 1001);
        }
        display();
        Scanner scan = new Scanner(System.in);
        int choice = scan.nextInt();
        while (choice != 5) {

            if (choice == 1) {
                printArray(a);
            } else if (choice == 2) {
                boolean flag = true;
                while (flag) {
                    flag = false;
                    for (int i = 0; i < a.length - 1; i++) {
                        if (a[i] > a[i + 1]) {
                            int temp = a[i];
                            a[i] = a[i + 1];
                            a[i + 1] = temp;
                            flag = true;
                        }
                    }
                }
                printArray(a);
            } else if (choice == 3) {
                System.out.println("Input number to search for:");
                int num = scan.nextInt();
                searchArray(a, num);
            } else if (choice == 4) {
                try {
                    Writer wr = new FileWriter("javaBasics.txt");
                    for (int i = 0; i < a.length; i++)
                        wr.write(a[i] + " ");
                    wr.close();
                } catch (IOException e) {
                    System.out.println("Error - " + e.toString());
                }
            } else {
                System.out.println("Please input a valid menu option...\n");
            }
            display();
            choice = scan.nextInt();
        }
    }

    static void printArray(int arr[]) {
        for (int i = 0; i < arr.length; i++) {
            System.out.println(arr[i] + " ");
        }
    }

    static void display() {
        System.out.println("1. Display the list of integers");
        System.out.println("2. Sort the list of integers");
        System.out.println("3. Search for a number");
        System.out.println("4. Save the list to an external file");
        System.out.println("5. Quit the program");
        System.out.print("Choice:");
    }

    static void searchArray(int arr[], int num) {
        boolean flag = false;
        for (int i = 0; i < arr.length; i++) {
            if (arr[i] == num) {
                System.out.println(num + " was found!");
                flag = true;
            }
        }
        if (flag == false) {
            System.out.println(num + " was not found");
        }
    }
}
```
