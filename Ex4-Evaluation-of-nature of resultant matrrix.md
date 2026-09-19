# Ex4 
## You are given a Java program that performs matrix addition. If Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension, what will be the nature (even/odd/mixed) of the resulting matrix?
## DATE: 16-09-2026
## AIM:
To write a java function to evaluate weather the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of resultant matrrix.

## Algorithm
1. Start the program.
2. Declare two 2D arrays, A and B, of the same size.
3. Initialize Matrix A with all odd numbers and Matrix B with all even numbers.
4. Create another 2D array C to store the sum of corresponding elements of A and B.
5. For each element position (i, j): `Compute C[i][j] = A[i][j] + B[i][j].`
   
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
Thus, the java program to evaluate weather the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of resultant matrrix is implemented successfully.
