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
import java.util.Scanner;

public class helloworld {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
        Scanner input = new Scanner(System.in);
        System.out.println("enter an integer: ");
        int number = input.nextInt();
        if(number % 5 == 0)
        {
        	System.out.println("HiFive");
        }
        if(number % 2 == 0)
        {
        	System.out.println("HiFive");
        }
	}

}

3-3
import java.util.Scanner;

public class helloworld {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		int number1 = (int)(Math.random() * 10);
		int number2 = (int)(Math.random() * 10);
		
		if (number1 < number2)
		{
			int temp = number1;
			number1 = number2;
			number2 = temp;
 		}
		
		System.out.print("what is" + number1 + " - " + number2 +"? ");
		Scanner input = new Scanner(System.in);
		int answer = input.nextInt();
		
		if(number1 - number2 == answer)
			System.out.println("You are correct!");
		else
		{
			System.out.println("Your answer is wrong.");
			System.out.println(number1 + " - " +number2 + " should be " + (number1 - number2));
		}
	}

}

3-4
import java.util.Scanner;

public class helloworld {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner input = new Scanner(System.in);
		System.out.print("Enter weight in pounds: ");
		double weight = input.nextDouble();
		System.out.print("Enter height in inches: ");
		double height = input.nextDouble();
		
		final double k = 0.45359237;
		final double m = 0.0254;
		
		double wk = weight * k;
		double hm = height * m;
		double bmi = wk / (hm * hm);
		
		System.out.println("BMI is " + bmi);
		if (bmi < 18.5)
			System.out.println("Underweight");
		else if (bmi < 25)
		{
			System.out.println("Normal");
		}
		else if(bmi < 30)
		{
			System.out.println("Overweight");
		}
		else
			System.out.println("Obese");
	}

}

3-5
import java.util.Scanner;

public class helloworld {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner input = new Scanner(System.in);
		System.out.print("(0-single filer,1-married jointly or)	" + "Qualifying widow(er),2-married separately,3-head of " + "household)Enter the filing status:");
		int status = input.nextInt();
		System.out.print("Enter the taxable income: ");
		double income = input.nextDouble();
		double tax = 0;
		
		if (status == 0)
		{
			if(income <= 8350)
			{
				tax = income * 0.1;
			}
			else if(income <= 33950)
			{
				tax = 8350 * 0.1 +(income- 8350) * 0.15 ;
			}
			else if(income <= 82250)
			{
				tax = 8350 * 0.1 +(33950- 8350) * 0.15 +(income - 33950) * 0.25 ;
			}
			else if(income <= 171550)
			{
				tax = 8350 * 0.1 +(33950- 8350) * 0.15 +(82250 - 33950) * 0.25 + (income -82250) *0.28 ;
			}
			else if(income <= 372950)
			{
				tax = 8350 * 0.1 +(33950- 8350) * 0.15 +(82250 - 33950) * 0.25 + (171550 -82250) *0.28 + (income -171550) * 0.33;
			}
			else 
			{
				tax = 8350 * 0.1 +(33950- 8350) * 0.15 +(82250 - 33950) * 0.25 + (171550 -82250) *0.28 + (372950 -171550) * 0.33 + (income - 372950) * 0.35;
			}
		}
		else if (status == 1)
		{
			if(income <= 16700)
			{
				tax = income * 0.1;
			}
			else if(income <= 67900)
			{
				tax = 16700 * 0.1 +(income- 16700) * 0.15 ;
			}
			else if(income <= 137050)
			{
				tax = 16700 * 0.1 +(67900- 16700) * 0.15 +(income - 67900) * 0.25 ;
			}
			else if(income <= 208850)
			{
				tax = 16700 * 0.1 +(67900 - 16700) * 0.15 +(137050 - 67900) * 0.25 + (income - 137050) *0.28 ;
			}
			else if(income <= 372950)
			{
				tax = 16700 * 0.1 +(67900 - 16700) * 0.15 +(137050 - 67900) * 0.25 + (208850 - 137050) *0.28 + (income - 208850) * 0.33;
			}
			else 
			{
				tax = 16700 * 0.1 +(67900 - 16700) * 0.15 +(137050 - 67900) * 0.25 + (208850 - 137050) *0.28 + (372950 - 208850) * 0.33 + (income - 372950) * 0.35;
			}
		}
		else if (status == 2)
		{
			if(income <= 8350)
			{
				tax = income * 0.1;
			}
			else if(income <= 33950)
			{
				tax = 8350 * 0.1 +(income- 8350) * 0.15 ;
			}
			else if(income <= 68525)
			{
				tax = 8350 * 0.1 +(33950- 8350) * 0.15 +(income - 33950) * 0.25 ;
			}
			else if(income <= 104425)
			{
				tax = 8350 * 0.1 +(33950- 8350) * 0.15 +(68525 - 33950) * 0.25 + (income -68525) *0.28 ;
			}
			else if(income <= 372950)
			{
				tax = 8350 * 0.1 +(33950- 8350) * 0.15 +(68525 - 33950) * 0.25 + (104425 -68525) *0.28   + (income -104425) * 0.33;
			}
			else 
			{
				tax = 8350 * 0.1 +(33950- 8350) * 0.15 +(68525 - 33950) * 0.25 + (104425 -68525) *0.28   + (186475 -104425) * 0.33 + (income - 186475) * 0.35;
			}
		}
		else if (status == 3)
		{
			if(income <= 11950)
			{
				tax = income * 0.1;
			}
			else if(income <= 45500)
			{
				tax = 11950 * 0.1 +(income- 11950) * 0.15 ;
			}
			else if(income <= 117450)
			{
				tax = 11950 * 0.1 +(45500 - 11950) * 0.15 + (income - 45500) * 0.25 ;
			}
			else if(income <= 190200)
			{
				tax = 11950 * 0.1 +(45500 - 11950) * 0.15 + (117450 - 45500) * 0.25 + (income - 117450) *0.28 ;
			}
			else if(income <= 372950)
			{
				tax = 11950 * 0.1 +(45500 - 11950) * 0.15 + (117450 - 45500) * 0.25 + (190200 - 117450) *0.28 + (income - 190200) * 0.33;
			}
			else 
			{
				tax = 11950 * 0.1 +(45500 - 11950) * 0.15 + (117450 - 45500) * 0.25 + (190200 - 117450) *0.28 + (372950 - 190200) * 0.33 + (income - 372950) * 0.35;
			}
		}
		else
		{
			System.out.println("Error: invalid status");
			System.exit(1);
		}
		System.out.println("Tax is " + (int)(tax * 100) /100.0);
	}

}

3-6
import java.util.Scanner;

public class helloworld {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner input = new Scanner(System.in);
		System.out.print("Enter an integer: ");
		int number = input.nextInt();
		
		if(number % 2 == 0 && number % 3 == 0)
		{
			System.out.println(number + " is divisible by 2 and 3.");
		}
		if(number % 2 == 0 || number % 3 == 0)
		{
			System.out.println(number + " is divisible by 2 or 3.");
		}
		if(number % 2 == 0 ^ number % 3 == 0)
		{
			System.out.println(number + " is divisible by 2 or 3, but not both.");
		}
	}

}

3-7
import java.util.Scanner;

public class helloworld {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner input = new Scanner(System.in);
		System.out.print("Enter a year: ");
		int year = input.nextInt();
		boolean isleapyear =
				(year % 4 == 0 && year % 100 !=0)||(year % 400 == 0);
		System.out.println(year + " is a leap year? " + isleapyear);
	}

}

3-8
import java.util.Scanner;

public class helloworld {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		int lottery = (int)(Math.random() * 100);
		
		Scanner input = new Scanner(System.in);
		System.out.print("Enter your lottery pick (two digits): ");
		int guess =input.nextInt();
		
		int lotterydigit1 = lottery / 10;
		int lotterydigit2 = lottery % 10;
		
		int guessdigit1 = guess / 10;
		int guessdigit2 = guess % 10;
		
		System.out.println("the lottery number is " + lottery);
		
		if(guess == lottery)
			System.out.println("Exact match:you win $10000");
		else if (guessdigit2 == lotterydigit1
				&&guessdigit1 == lotterydigit2)
			System.out.println("Match all digits");
		else if(guessdigit1 == lotterydigit1
				||guessdigit1 == lotterydigit2
				||guessdigit2 == lotterydigit1
				||guessdigit2 == lotterydigit2)
			System.out.println("Match one digit");
		else
			System.out.println("sorry, no match");
	}

}

3-9
import java.util.Scanner;

public class helloworld {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner input = new Scanner(System.in);
		System.out.print("Enter a year: ");
		int year = input.nextInt();
		
		switch (year % 12)
		{
		case 0:System.out.println("monkey");break;
		case 1:System.out.println("rooster");break;
		case 2:System.out.println("dog");break;
		case 3:System.out.println("pig");break;
		case 4:System.out.println("rat");break;
		case 5:System.out.println("ox");break;
		case 6:System.out.println("tiger");break;
		case 7:System.out.println("rabbit");break;
		case 8:System.out.println("dragon");break;
		case 9:System.out.println("snake");break;
		case 10:System.out.println("horse");break;
		case 11:System.out.println("sheep");break;
		}
	}

}
