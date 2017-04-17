# Calculator
# Basics operations of calculator: Addition/Subtraction/Divition/Multiplication

package com.inportia;

import java.util.Scanner;

public class Calculator {
	
	static Scanner in;

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		int flag=0;
		
		do{
			int result = 0;
			System.out.println("Following program will perform" + "1. Addition 2. Substraction 3. Multiplication 4. Division");
			System.out.println("Enter your choice in iteger");
			
			int choice = takeInput();
			
			switch(choice){
			case 1: 
					result = add();
					break; // breaks the case otherwise it will give output for all cases
			case 2:
					result = subtract();
					break;
			case 3: 
					result = multiply();
					break;
			case 4: 
					result = division();
					break;
			default:
					System.out.println("Invalid choice");
			}
			System.out.println(result);
			System.out.println("Do you want to continue (1/0)");
			flag = takeInput();
			
		}while(flag==1);
			in.close();
			
		}
	
	private static int division() {
		// TODO Auto-generated method stub
		System.out.println("division");
		int num1 = takeInput();
		int num2 = takeInput();
		return num1/num2;
	}

	private static int multiply() {
		// TODO Auto-generated method stub
		System.out.println("multiply");
		int num1 = takeInput();
		int num2 = takeInput();
		return num1*num2;
	}

	private static int subtract() {
		// TODO Auto-generated method stub
		System.out.println("subtract");
		int num1 = takeInput();
		int num2 = takeInput();
		return num1-num2;
	}

	private static int add() {
		// TODO Auto-generated method stub
		System.out.println("add");
		int num1 = takeInput();
		int num2 = takeInput();
		return num1+num2;
	}
	
	private static int takeInput(){
		System.out.println("Enter Number: ");
		in = new Scanner (System.in);
		int num =in.nextInt();
		return num;
	}
	
}

