# JAVA_DS_Module-6 — Combined File

This document combines all files in the repository into one PDF-friendly report.

---

# EX 1
## You’re creating a health monitoring device which stores several sensor readings in an array. To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.
## DATE: 16.9.2026
## AIM:
To write a JAVA program to determine the minimum value (e.g., lowest heartbeat), implementing a recursive method.

## Algorithm
1. Start the program.
2. Read the number of elements and store them in an array.
3. Define a recursive function `findMin()` that compares elements to find the minimum.
4. Base condition: If the array has one element, return that element.
5. Recursive step: Compare the last element with the minimum of the rest of the array and return the smaller one.
6. Display the minimum value.
7. Stop the program.

## Program:
```java
/*
Program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.
Developed by:  Abinaya A
Register Number: 212224230004
*/

import java.util.*;

public class Main {
    static int getMin(int[] arr, int i, int n) {
        if (i == n - 1) {
            return arr[i];
        }
        int minRest = getMin(arr, i + 1, n);
        return Math.min(arr[i], minRest);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }
        System.out.println(getMin(arr, 0, n));
    }
}
```

## Output:
<img width="405" height="177" alt="image" src="https://github.com/user-attachments/assets/22087b27-b119-42b0-90cc-cd6e365863d6" />

## Result:
Thus the JAVA program to find the minimum value (e.g., lowest heartbeat), implementing a recursive method, has been implemented successfully.

---

# EX2
## Count how many times a number appears in an array recursively.
## DATE: 16-09-2026
## AIM:
To write a Java program to count how many times a number appears in an array recursively.

## Algorithm
1. Start the program.
2. Read the number of elements and store them in an array.
3. Get the number to be counted from the user.
4. Define a recursive function `countOccurrences()` to count occurrences.
5. Use base and recursive conditions to count occurrences.
6. Display the result.
7. Stop the program.

## Program:
```java
/*
Program Count how many times a number appears in an array recursively.
Developed by: Abinaya A
Register Number: 212224230004
*/

import java.util.Scanner;

public class CountOccurrencesRecursive {
    static int countOccurrences(int arr[], int n, int key) {
        if (n == 0)
            return 0;
        return (arr[n - 1] == key ? 1 : 0) + countOccurrences(arr, n - 1, key);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter number of elements: ");
        int n = sc.nextInt();
        int arr[] = new int[n];
        System.out.println("Enter the elements:");
        for (int i = 0; i < n; i++)
            arr[i] = sc.nextInt();
        System.out.print("Enter number to count: ");
        int key = sc.nextInt();
        System.out.println("The number " + key + " appears " + countOccurrences(arr, n, key) + " times.");
        sc.close();
    }
}
```

## Output:
<img width="985" height="540" alt="image" src="https://github.com/user-attachments/assets/397a8639-8e9d-4bef-bb30-0a95baa40eb9" />

## Result:
Thus, the Java program to count how many times a number appears in an array recursively is implemented successfully.

---

# Ex3
## Write a program to count the number of digits in an integer.
## DATE: 16-09-2026
## AIM:
To write a Java program to count the number of digits in an integer.

## Algorithm
1. Start the program.
2. Declare an integer variable `n` and `count = 0`.
3. Read the integer number `n` from the user.
4. If `n` is 0, then the count of digits is 1.
5. Otherwise, repeat while `n != 0`; divide by 10 and increment the count.
6. Display the value of count.
7. Stop the program.

## Program:
```java
/*
Program to count the number of digits in an integer
Developed by: Abinaya
Register Number: 212224230004
*/

import java.util.Scanner;

public class CountDigits {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num, count = 0;

        System.out.print("Enter an integer: ");
        num = sc.nextInt();

        if (num == 0) {
            count = 1;
        } else {
            while (num != 0) {
                num = num / 10;
                count++;
            }
        }

        System.out.println("Number of digits: " + count);
        sc.close();
    }
}
```

## Output:
<img width="543" height="180" alt="image" src="https://github.com/user-attachments/assets/2e4cd75f-cb9c-461e-a79c-e7dec98ff288" />

## Result:
Thus, the Java program to count the number of digits in an integer is implemented successfully.

---

# Ex4
## You are given a Java program that performs matrix addition. If Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension, what will be the nature (even/odd/mixed) of the resultant matrix?
## DATE: 16-09-2026
## AIM:
To write a Java function to evaluate whether the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of the resultant matrix.

## Algorithm
1. Start the program.
2. Declare two 2D arrays, `A` and `B`, of the same size.
3. Initialize Matrix A with odd numbers and Matrix B with even numbers.
4. Create another 2D array `C` to store the sum of corresponding elements of A and B.
5. For each element position `(i, j)`, compute `C[i][j] = A[i][j] + B[i][j]`.

## Program:
```java
/*
Program to find the nature of resultant matrix.
Developed by: Abinaya A
Register Number: 212224230004
*/

import java.util.*;
public class Main{
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);

        int a=sc.nextInt();
        int b=sc.nextInt();
        int[][] row=new int[a][b];
        int[][] col=new int[a][b];
        int[][] res=new int[a][b];
        for(int i=0;i<a;i++){
            for(int j=0;j<b;j++){
                row[i][j]=sc.nextInt();
            }
        }

        for(int i=0;i<a;i++){
            for(int j=0;j<b;j++){
                col[i][j]=sc.nextInt();
            }
        }

        for(int i=0;i<a;i++){
            for(int j=0;j<b;j++){
                res[i][j]=row[i][j]+col[i][j];
            }
        }

        for(int i=0;i<a;i++){
            for(int j=0;j<b;j++){
                System.out.print(res[i][j]);
                if(j<b-1){
                    System.out.print(" ");
                }
            }
            System.out.println();
        }
    }
}
```

## Output:
<img width="374" height="546" alt="image" src="https://github.com/user-attachments/assets/6f43e89f-7342-4e0d-aefe-68099b7b7546" />

## Result:
Thus, the Java program to evaluate whether the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and to find the nature of the resultant matrix is implemented successfully.

---

# Ex5
## Count Inversions in an Array
## DATE: 16-09-2026
## AIM:
To write a Java program to count the number of inversions in an array where inversion is defined as: `arr[i] > arr[j]` and `i < j`.

## Algorithm
1. Start the program.
2. Declare an array `arr[]` and a variable `count = 0` to store the number of inversions.
3. Read the array elements from the user.
4. For each pair of elements `(arr[i], arr[j])`, check if `arr[i] > arr[j]` and `i < j`.
5. If the above condition is true, increment the inversion count.
6. Continue until all pairs are checked.
7. Display the total number of inversions found in the array and stop the program.

## Program:
```java
/*
Program to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j
Developed by:Abinaya A
Register Number: 212224230004
*/

import java.util.Scanner;

public class CountInversions {
    public static int mergeSortAndCount(int[] arr, int left, int right) {
        int count = 0;
        if (left < right) {
            int mid = (left + right) / 2;
            count += mergeSortAndCount(arr, left, mid);
            count += mergeSortAndCount(arr, mid + 1, right);
            count += mergeAndCount(arr, left, mid, right);
        }
        return count;
    }

    private static int mergeAndCount(int[] arr, int left, int mid, int right) {
        int[] leftArr = new int[mid - left + 1];
        int[] rightArr = new int[right - mid];

        for (int i = 0; i < leftArr.length; i++) leftArr[i] = arr[left + i];
        for (int i = 0; i < rightArr.length; i++) rightArr[i] = arr[mid + 1 + i];

        int i = 0, j = 0, k = left, swaps = 0;

        while (i < leftArr.length && j < rightArr.length) {
            if (leftArr[i] <= rightArr[j]) {
                arr[k++] = leftArr[i++];
            } else {
                arr[k++] = rightArr[j++];
                swaps += (leftArr.length - i);
            }
        }

        while (i < leftArr.length) arr[k++] = leftArr[i++];
        while (j < rightArr.length) arr[k++] = rightArr[j++];

        return swaps;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) arr[i] = sc.nextInt();
        System.out.println(mergeSortAndCount(arr, 0, n - 1));
    }
}
```

## Output:
<img width="357" height="240" alt="image" src="https://github.com/user-attachments/assets/2fd053aa-21d5-439b-8af8-78fb80123460" />

## Result:
Thus, the Java program to count the number of inversions in an array where `arr[i] > arr[j]` and `i < j` is implemented successfully.

---

# Conclusion
This repository contains five Java programming exercises focused on recursion, counting, matrix operations, and inversion counting. The combined document is ready to be exported to PDF.
