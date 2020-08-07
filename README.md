# Tasks 1-3

## Task 1 A

```java
//*************************************//
//* StudentID: 1812103                 //
//* Date: 23.07.2020                   //
//* Task: 1a                           //
//* Description: Testing the basic     //
//* primitives and operations of Java  //
//*************************************//
package Task1a;
//importing the java.util package so I can use the util.Scanner
import java.util.Scanner;

public class Task1a {

	//Declaring and explicitly initialising the class instance fields
	private static int numberOne = 0; 
	private static int numberTwo = 0;
	private static int muxRes = 0;
	
	/*the main method is used to execute the program and since it is public,
	it allows for global visability. It also does not need to instantiate
	an object to have a reference*/
	public static void main(String[] args) 
	{
	//the scanner method allows you to store the users input into the MyInput variable 
	Scanner input = new Scanner(System.in);
	//asking the user for input through the println command which prints in java
	//getting the first integer inputted from memory location by the user
	System.out.println("Enter a number: ");
	numberOne = input.nextInt();
	//getting the second integer from the users memory location
	//using println to print the line in java
	System.out.println("Enter a number: ");
	numberTwo = input.nextInt();
	
	//The system will multiply the two integers together using the multiplication
	// operator and storing it within the muxRes variable
	muxRes = numberOne * numberTwo;
	
	//Display the multiplication result of numberOne and numberTwo to the user
	System.out.println("The new number is: ");
	System.out.println(muxRes);
	}
}
```

## Task 1  B

```java
//**************************************//
//* StudentID: 1812103                  //
//* Date: 25.07.2020                    //
//* Task: 1b                            //
//* Description: 3 integer Calculator   //
//**************************************//

//importing the java.util API to be able to use the util.Scanner
import java.util.Scanner;

public class Task1b {
		//using the Scanner from the java library
		//initialising and declaring the class instance fields
		//this class is public, therefore allowing it to be accessed by objects, classes and packages
		private static int numberOne = 0;
		private static int numberTwo = 0;
		private static int numberThree = 0;
		private static double average = 0;
		
		//declaring the object input of class Scanner
		private static Scanner input;
		
			public static void main(String[] args) {
			//using the scanner class to achieve user input
			//this will be stored in the Scanner input object
			Scanner input = new Scanner(System.in);
		
				//asking the user to input the first integer from the memory location in input
				System.out.println("Please input your first number: ");
				int numberOne = input .nextInt();
				//asking the user for the second integer from the input location
				System.out.println("Please input your second number: ");
				int numberTwo = input .nextInt();
				//asking the user for the third integer
				System.out.println("Please input your third number: ");
				int numberThree = input .nextInt();
		
		
				/*using less than and more than operators to figure out the order of all the integers, and the order they are printed
				 whether they are first, second or third. This is done with if, else if conditional statements to figure out which 
				are the largest and the smallest integers when they are entered by the user*/
				//when the statements have organised the integers into the correct descending order, the system prints them using Println
				if ((numberOne > numberTwo && numberOne > numberThree) & (numberTwo > numberThree))
				{	
				System.out.println("The correct decsending order is: " + numberOne + ", " + numberTwo + ", " + numberThree);
				}
				else if ((numberOne > numberTwo && numberOne > numberThree) & (numberThree > numberTwo))
				{
				System.out.println("The correct descending order is: " + numberOne + ", " + numberThree + ", " + numberTwo);
				} 
				else if ((numberTwo > numberOne && numberTwo > numberThree) & (numberOne > numberThree))
				{
				System.out.println("The correct descending order is: " + numberTwo + ", " + numberOne + ", " + numberThree);
				}
				else if ((numberTwo > numberOne && numberTwo > numberThree) & (numberThree > numberOne))
				{
				System.out.println("The correct descending order is: " + numberTwo + ", " + numberThree + ", " + numberOne);
				}
				else if ((numberThree > numberOne && numberThree > numberTwo) & (numberOne > numberTwo))
				{
				System.out.println("The correct descending order is:" + numberThree + ", " + numberOne + ", " + numberTwo);
				}
				else if ((numberThree > numberOne && numberThree > numberTwo) & (numberTwo > numberOne))
				{
				System.out.println("The correct descending order is: " + numberThree + ", " + numberTwo + ", " + numberOne);
				}
				/*if the integers were enterd incorrectly or they were of the same value, the system outputs an invalid message to the user*/
				else 
				{
				System.out.println("Numbers are all equal or invalid entry");
				}
		
				//since there are 3 integers, you can achieve the average by using the divison operator
				average = (numberOne + numberTwo + numberThree) / 3;
		
					//The system prints the averages to the user by using println
				System.out.println("The average of these numbers added together is " + average); 
		}// end method
}// end class
```

# Task 2

## Task 2 A

### PrintAccount.java

```java
//*************************************//
//* StudentID: 1812103                 //
//* Date: 29.07.2020                   //
//* Task: 2a                           //
//* Description: PrintAccount.java      //
//*                                    //
//*************************************//

/*there is no main method for this class since it is ran from PrintAccountTest. This is because
its main responsibility is storing the methods for an object when then are initialised  */
public class PrintAccount
{

	//declare the class instance fields
	public String name;
	public double balance;
	
	public String getName() 
	{
	//this returns the set name to the object
		return name;
	}
	
	public void setName(String name) 
	{
	//this is used to set the name of the String name
	//the String name is this.name and "name" is the name within the method
		this.name = name;
	}
	//public PrintAccount constructor and is used to construct objects when 
	//they are created in another class
	public PrintAccount(double balance) 
	{
		if (balance >= 0.0)
		{
			this.balance = balance;
		}
		//in case of an incorrect balance, the system will display the invalid output 
		//using println to the user
		else 
		{
			System.out.println("Invalid balance");
		}
	}
	//using a public void will not return the value
	public void payIn(double amount) 
	{
		//adds the amount paid into the account onto the original balance
		balance = balance + amount;
	}
	//gets the balance of the double balance variable and then will return it
	public double getBalance() 
	{
		//after the method is used, the balance is returned
		return balance;
	}
}
```

### PrintAccountTest.java

```java
//*************************************//
//* StudentID: 1812103                 //
//* Date: 29.07.2020                   //
//* Task: 2a                           //
//* Description: PrintAccountTest.java //
//*                                    //
//*************************************//
import java.util.Scanner;

public class PrintAccountTest
//this is the main method that is used to implement the java program
{
	public static void main(String[] args) 
	{
		/*creating User 1 from PrintAccount.java and setting a specific set
		balance from constructor*/
		PrintAccount UserOne = new PrintAccount(0.00);
		//using the payIn method previously used in PrintAccount.java to minus 
		//120.00 from object User 1 
		UserOne.payIn(27.00);
		//this uses the setter from PrintAccount object and sets the default name to User 1
		UserOne.setName(" ");
		//creating a new object for User 2 with a set balance from the PrintAccount constructor
		PrintAccount UserTwo = new PrintAccount(0.00);
		//using the payIn method to minus 120.00 from object User 2
		UserTwo.payIn(-120.00);
		//setting the default name to User 2 using the method setName from PrintAccount
		UserTwo.setName(" ");
		//asking for user input by using the getName method for User 1
		System.out.printf(UserOne.getName() + "Enter name of User 1: ");
		//using Scanner class to achieve user input
		Scanner userInput = new Scanner(System.in);
		//setting User 1 as the next memory location in input variable
		UserOne.setName(userInput.nextLine());
		//prints the users name and balance
		System.out.printf(UserOne.getName() + " has a balance of " + UserOne.getBalance());
		//setting the next input variable onto the next line, the user will have to press enter to continue
		UserTwo.setName(userInput.nextLine());
		//getting the name of User 2 with the getName method
		System.out.printf(UserTwo.getName() + "Enter name of User 2: ");
		//sets the name of User 2 using setName method and sets next memory location
		UserTwo.setName(userInput.nextLine());
		//closing the scanner
		userInput.close();
		//prints users name and balance
		System.out.printf(UserTwo.getName() + " has a balance of " + UserTwo.getBalance());
	}
}
```

## Task 2 B

### PrintAccount2.java

```java
//*************************************//
//* StudentID: 1812103                 //
//* Date: 06.08.2020                   //
//* Task: 2b                           //
//* Description: PrintAccount2.java    //
//*                                    //
//*************************************//

public class PrintAccount2 {

		//declaring and initiating variables
		public String name;
		public double balance;
		
		//getName method
		public String getName()
		{
			//returns the name and object
			return name;
		}
		
		//setting the name method from the variable string
		public void setName(String name)
		{
			this.name = name;
		}
		//create PrintAccount object with name and balance through using a constructor
		public PrintAccount2(double balance , String name) 
		{
			this.name = name;
			if (balance >= 0.0)
			{
				this.balance = balance;
			}
			//if balance is invalid or incorrect, an invalid message will appear to the user
			//through the use of println
			else 
			{
				System.out.println("Invalid balance");
			}
		}
		//does not return the value since it is a public void
		public void payIn(double amount) 
		{
			balance = balance + amount;
		}
		//returns the balance once it obtains the double balance variable
		public double getBalance() 
		{
			return balance;
		}
	}

```

### PrintAccountTest2.java

```java
//**************************************//
//* StudentID: 1812103                  //
//* Date: 06.08.2020                    //
//* Task: 2b                            //
//* Description: PrintAccountTest2.java //
//*                                     //
//**************************************//

//importing and declaring the javax.swing package
import javax.swing.*;

public class PrintAccountTest2 {
	//declaring the string types and the class instance fields
	public static String BalanceOne, BalanceTwo;
	public static double OneTransaction, TwoTransaction, tempTwo, tempOne;
	public static String NameOne, NameTwo;

	//the main method
	public static void main(String[] args) {
		//creating three JFrames from the API to be objects
		JFrame frameOne = new JFrame("what is the name of customer 1?:");
		JFrame frameTwo = new JFrame("what is the balance of customer 1?:");
		JFrame frameThree = new JFrame("what is the name of customer 2?:");
		//obtaining the input from the customer and storing it within the variable NameOne
		NameOne = JOptionPane.showInputDialog(frameOne, "name of customer 1:");
		
		BalanceOne = JOptionPane.showInputDialog(frameTwo, "What is " + NameOne + " current balance?:");
		
		//obtaining the input from customer 2 and storing it as NameTwo 
		NameTwo = JOptionPane.showInputDialog(frameOne, "what is the name of customer 2?");
		
		BalanceTwo = JOptionPane.showInputDialog(frameTwo, "What is " + NameTwo + " current balance?:");
		
		//creating an object for customer 1 and 2 and obtaining the inputs
		//parsing the amounts with the constructor method
		PrintAccount2 custOne = new PrintAccount2(Double.parseDouble(BalanceOne), NameOne);
		PrintAccount2 custTwo = new PrintAccount2(Double.parseDouble(BalanceOne), NameTwo);
		//asking customers how much they would like to pay in through making a fourth JFrame
		JFrame frameFour = new JFrame("Hi" + custTwo.getName());
		
		//obtaining customer input and storing it within the string variable
		String tempFour = String.valueOf(OneTransaction);
		
		//asking for customer input and transaction being read from payIn method
		tempFour = JOptionPane.showInputDialog(frameThree,
				"what is the amount you would like to pay in , " + custOne.getName());
		
		tempOne = Double.parseDouble(tempFour);

		String tempThree = String.valueOf(TwoTransaction);
		
		
		tempThree = JOptionPane.showInputDialog(frameFour,
				"what is the amount you would like to pay in , " + custTwo.getName());
		tempTwo = Double.parseDouble(tempThree);
		
		//customers use payIn method to complete transaction to accounts 
		custOne.payIn(tempOne);
		custTwo.payIn(tempTwo);
		
		//displaying the users names and balances in double and string instance fields
		JOptionPane.showMessageDialog(null, custOne.getName() + "balance is " + custOne.getBalance());
		JOptionPane.showMessageDialog(null, custTwo.getName() + "balance is " + custTwo.getBalance());
	}
}

```

# Task 3

## Task 3 A

### CourseStats.java

```java
//*************************************//
//* StudentID: 1812103                 //
//* Date: 06.08.2020                   //
//* Task: 3a                           //
//* Description: CourseStats.java      //
//*                                    //
//*************************************//

import java.util.Scanner;

public class CourseStats {
	//declaring and initialising the integers for student passes, 
	//failures and overall grade amount
	public static int passes = 0;
	public static int failures = 0;
	public static int overallGrade;
	
	private static Scanner scan;
	
	public static void main(String[] args) {
		//initialising the student counter for while loop
		int studentCounter = 1;
		
		scan = new Scanner(System.in);
		//loop until the student counter is less than or equal to 40
		while (studentCounter <= 40) {
			//Getting user input for student's grade
			System.out.println("Enter Student" + studentCounter + "'s " + "Grade");
			//getting user input as the integer
			overallGrade = scan.nextInt();
		//if the grade is equal to 1, then 1 is added to the passes amount	
		if (overallGrade == 1) {
			passes++;
			}
		//if the grade is equal to 0, then 0 is added to the failures amount	
		else if (overallGrade ==0) {
			failures++;
			}
		//the studentCounter will loop again once the grade from each student is added
		studentCounter++;
		
		}
	scan.close();
	//the system outputs the number of passes while using println
		
	System.out.println("The number of passes within the class was: " + passes);
	//the system outputs the number of failures while using println
	System.out.println("The number of failures within the class was: " + failures);
	
		//if passes are more than 32
		if (passes > 32) {
			//the system will output a message to the tutors
			System.out.println("Congratulations to the Tutors!");
	}
		}
}
```

## Task 3 B

### CourseStats.java

```java
//*************************************//
//* StudentID: 1812103                 //
//* Date: 06.08.2020                   //
//* Task: 3b                           //
//* Description: CourseStats.java      //
//*                                    //
//*************************************//

//importing and declaring the javax swing packages
import javax.swing.JFrame;
import javax.swing.JOptionPane;

public class CourseStats {
	//declaring and initialising the integers for student passes, 
	//failures and overall grade amount
	public static int passes = 0;
	public static int failures = 0;
	public static int overallGrade;
	//initialising a string type for message
	public static String message = " ";
	
	//the main method
	public static void main(String[] args) 
	{
		//initialising the student counter for while loop
		int studentCounter = 1;
	//creating a new JFrame object from the javax package
	JFrame frame = new JFrame();
		
	//if the student counter is less than or equal to 40, use parse string from the input
	while (studentCounter <= 40) 
	{
		//Getting user input for student's grade
		overallGrade = Integer
				.parseInt(JOptionPane.showInputDialog(frame, "Enter Student" + studentCounter + "'s " + "Grade"));
			
	//if the grade is equal to 1, then 1 is added to the passes amount	
	if (overallGrade == 1) 
		{
		passes++;
		}
	//if the grade is equal to 0, then 0 is added to the failures amount	
	else if (overallGrade ==0) 
		{
		failures++;
		}
	//the studentCounter will loop again once the grade from each student is added
	studentCounter++;
		
	}
		//if there are more than 32 students that have passed
	if (passes > 32) 
		{
		//the system will output a message to the tutors
		message = ("Congratulations to the Tutors!");
		}
	//JOptionPane is used to show the message containing the number of passes and failures	
	JOptionPane.showMessageDialog(frame, "The number of passes within the class was: " + passes + "\n" + "The number of failures within"
				+ " the class was: " + failures + "\n" + message);
	}
}
```
