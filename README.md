# java-unit-3

3-1
package hello;

import java.util.Scanner;

public class helloo {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		int number1 = (int)(System.currentTimeMillis() % 10);
		int number2 = (int)(System.currentTimeMillis() / 7 % 10);
		Scanner input = new Scanner(System.in);
		System.out.print("what is" + number1 + " " + number2 + "? ");
		int answer = input.nextInt();
		System.out.println(number1 + " + " + number2 + " = " + answer + " is " + (number1 +number2 == answer));
        }
}

3-2
