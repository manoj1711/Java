package com.company;

import java.util.Scanner;

public class UsernameValidation {
    public static void main(String[] args) {
        System.out.println("Enter Username :");
        Scanner scanner = new Scanner(System.in);
        String s1 = scanner.nextLine();
          int n = Validation(s1);
          if(n == 1){
              System.out.println("It is a valid Username");
          }
          else {
              System.out.println("It is not a valid Userame");
          }
    }

    private static int Validation(String s1) {
        if(s1.matches(".*[0-9]{1,}.*") && s1.matches(".*[@#$]{1,}.*") && s1.length() >=6 && s1.length()<=20){
            return  1;
        }
        else
        {
            return -1;
        }
    }
}
