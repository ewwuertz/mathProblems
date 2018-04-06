# mathProblems
#include <iostream>
#include <conio.h>
#include <cstdlib>
#include <ctime>
#include <iomanip>
using namespace std;

int main()
{
	int choice,
	      num1,
	      num2,
	      answer, // answer to the problem
                          sum;
	// Seed the random number generator.
	srand((unsigned)time(0));

	num1 = rand() % 100;
	num2 = rand() % 100;
	do
	{
		cout << "\tMath Tutor Menu\n";
		cout << "-----------------------------------------" << endl;
		cout << "1. Addition problem" << endl;
		cout << "2. Subtraction Problem" << endl;
		cout << "3. Multiplication Problem" << endl;
		cout << "4. Division problem" << endl;
		cout << "5. Quit this program" << endl;
		cout << "------------------------------------------" << endl;
		cout << "Enter your coice (1-5): ";
		cin >> choice;

		switch (choice)
		{
		case 1: //the addition case
			//added setw to make it look slightly cleaner
			cout << setw(5) << num1 << endl;
			cout << "+"<< setw(4) << num2 << endl;
			cout << "-----" << endl;
			cout << setw(2) << " ";
			cin >> sum;
			answer = num1 + num2;
			if (sum == answer)
				cout << "\n\nCongratulations! That's right.\n" << endl;
			else
				cout << "\n\nSorry the correct answer is " << answer <<"." << endl;
			break;

		case 2: //the subtraction case
			//added setw to make it look slightly cleaner
			cout << setw(5) << num1 << endl;
			cout << "-" << setw(4) << num2 << endl;
			cout << "-----" << endl;
			cout << setw(2) << " ";
			cin >> sum;
			answer = num1 - num2;
			if (sum == answer)
				cout << "\n\nCongratulations! Thats right.\n" << endl;
			else
				cout << "\n\nSorry the correct answer is " << answer << ".\n" << endl;
			break;

		case 3: //the multiply case
			cout << num1 << " * " << num2 << " = ";
			cin >> sum;
			answer = num1*num2;
			if (sum == answer)
				cout << "Congratultionts! Thats right!" << endl;
			else
				cout << "Sorry the correct answer is " << answer << "." << endl;
			break;

		case 4: //the division case
			cout << "\n\n " << num1 << " / " << num2 << " = ";
			cin >> sum;
			answer = num1 / num2;
			if (sum == answer)
				cout << "Congratulations! Thats right!" << endl;
			else
				cout << "Sorry the correct answer is " << answer << "." << endl;
			break;
		case 5: //user decides to quit
			cout << "Thank you for using Math Tutor." << endl;
			break;
		default: //user inputs a number >5 or less <1
			cout << "The valid choices are 1,2,3,4,5. Please enter your choice: " << endl;
			cin >> choice;
			break;
		}

	} while (choice>0 && choice <= 4);
	cout << "Thank you for using the math tutor." << endl;
	_getch();//pause system
	return 0;
}
