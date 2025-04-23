# BMI Calculator - Java

This is a simple **Body Mass Index (BMI) Calculator** written in Java. The program takes user input for **weight in pounds** and **height in meters**, calculates the BMI, and categorizes the result based on standard BMI ranges.

---

## ⚠️ Note

The code snippet includes a minor bug:
```java
private static int height;
This variable is never assigned a value, but is used in the BMI calculation. It should be removed or replaced with the correct heightinmeters variable:

java
Copy
Edit
double bmi = weightinkgs / (heightinmeters * heightinmeters);
Make sure to fix this before running the program.

📁 Program Structure
java
Copy
Edit
public class BMICalculator {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Enter your weight in Pounds:");
        double weightinPounds = scanner.nextDouble();

        System.out.println("Enter your height in meters:");
        double heightinmeters = scanner.nextDouble();

        double weightinkgs = weightinPounds * 0.453592;
        double bmi = weightinkgs / (heightinmeters * heightinmeters);

        System.out.println("Your BMI is: " + bmi);

        if (bmi < 18.5) {
            System.out.println("You are underweight");
        } else if (bmi >= 18.5 && bmi < 24.9) {
            System.out.println("You are a healthy weight");
        } else if (bmi >= 25 && bmi < 29.9) {
            System.out.println("You are overweight");
        } else {
            System.out.println("You are obese");
        }

        scanner.close();
    }
}
📊 What is BMI?
BMI (Body Mass Index) is a simple calculation using a person's height and weight:

ini
Copy
Edit
BMI = weight (kg) / height² (m²)
🧑‍💻 How to Compile and Run
Using Terminal:
bash
Copy
Edit
javac BMICalculator.java
java BMICalculator
✅ Requirements
Java JDK 8 or higher

Terminal or IDE like Eclipse, IntelliJ, or VS Code with Java support

🧠 Categories

BMI Range	Category
Less than 18.5	Underweight
18.5 – 24.9	Healthy Weight
25 – 29.9	Overweight
30 or more	Obese
