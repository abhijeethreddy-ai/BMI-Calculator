# BMI-Calculator

ackage day4;

import java.util.Scanner;

public class bmicalculatorfinal {

	private static int height;

	public static void main(String[] args) {
		// TODO Auto-generated method stub

		Scanner scanner = new Scanner(System.in);

		System.out.println("Enter your weight in Pounds");

		double weightinPounds = scanner.nextDouble();

		System.out.println("Enter your height in meters");

		double heightinmeters = scanner.nextDouble();

		double weightinkgs = weightinPounds * 0.453592;

		double bmi = weightinkgs / (height * height);

		System.out.println("Your BMI is: "+ bmi);

		if (bmi<18.5)

		{
			System.out.println("Your are under weight");
		}

		else if (bmi >= 18.5 && bmi < 24.9) {

			System.out.println("You are Healthy Weight");
		}

		else if (bmi >= 25 && bmi < 29.9)

		{
			System.out.println("Your are Over weight");

		}

		else

		{
			System.out.println("Your are Obese");

		}
scanner.close();
	}

}
