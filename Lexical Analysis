package Experiment_1;

import java.util.ArrayList;
import java.util.HashMap;
import java.util.Map;
import java.util.Scanner;

public class LexicalAnalysis {

    public static void main(String[] args) {

        String[] id = new String[25];
        int a=0;// index of the array
        for (char i = 'a'; i < 'z'; i++) {
            id[a] = String.valueOf(i);
            a++;
        }

        String[] operator = {"+","-","*","/","<",">"};

        int n = 10000;
        String[] literal = new String[n];                       // Declaraion of litral array
        for (int i = 0; i < literal.length; i++) {
            literal[i] = String.valueOf(i + 1);
        }

        String[] keyword = { "and", "break", "continue", "class", "else if", "else", "except", "finally", "for","if", "not",
                "or", "try", "while", "do", "catch"};

        String[] symbol = {"!","=","@",";","%","(",")","{","}"};
        Scanner in = new Scanner(System.in);

        System.out.println("Enter the expression with space after each character");
        System.out.println("Eg. if ( a > 10 ) + a");
        String input = in.nextLine();
//        String input = "if ( a > b ) + a - b + 1";

        String[] toStringArray = null;
        toStringArray = input.split(" ");

        int idCounter = 0;

        String[] storeId = new String[idCounter];
        int symbolCounter = 1;
        ArrayList<String> temp = new ArrayList<>(); // Declaration of dynamic array
        for (int i = 0; i < toStringArray.length; i++) {
            for (String s : id) {

                String val = toStringArray[i];
                if (val.equals(s)) {
                    if (!temp.equals(val)){
                        temp.add(val);
                        int idCount = temp.indexOf(val)+1;
                        System.out.println(temp.get(temp.indexOf(val)) +" --> id "+idCount);
                    }

                }
            }
            for (String s : operator) {
                if (toStringArray[i].equals(s)) {
                    System.out.println(toStringArray[i] + " -> operator");
                }
            }
            for (String s : literal) {
                if (toStringArray[i].equals(s)) {
                    System.out.println(toStringArray[i] + " -> literal");
                }
            }
            for (String s : keyword) {
                if (toStringArray[i].equals(s)) {
                    System.out.println(toStringArray[i] + " -> keyword");
                }
            }
            for (String s : symbol) {
                if (toStringArray[i].equals(s)) {
                    System.out.println(toStringArray[i] + " -> symbol " + symbolCounter);
                    symbolCounter++;
                }
            }
        }
    }
}
