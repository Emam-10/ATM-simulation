# ATM-simulation
ATM-simulation using C++
#include <iostream>
using namespace std;

//********variable*******//
double balance = 1000;
int deposit = 0;
int withdraw = 0;
int password = 1234;
int choice = 0;

//***************************


void show()
{
	cout << "********Menu*********" << endl;
	cout << "1:Balance" << endl;
	cout << "2:Withdraw" << endl;
	cout << "3:Deposit" << endl;
	cout << "4:Exit" << endl;
	cout << "*************************\n";
}

void process()
{
	cout << "Please enter the password" << endl;
	cin >> password;
	do {
	if (password == 1234)
	{
		cout <<"Enter your choice" << endl;
		cin >> choice;
		
		
			switch (choice)
			{
			case 1:
				cout << "The Balance is " << balance << endl;
				break;


			case 2:
				cout << " Note : Your Balance is " << balance << endl;
				cout << "Enter the amount " << endl;
				cin >> withdraw;
				if (withdraw > balance) {

					cout << "sorry you can't withdraw this amount" << endl;

				}
				else {

					balance -= withdraw;
					cout << "Now : Your Balnace is " << balance << endl;

					break;
				}

			case 3:
				cout << "Note : Your Balance is " << balance << endl;
				cout << "Please eneter your Deposit money " << endl;
				cin >> deposit;
				balance += deposit;
				cout << "Your new Balance is " << balance << endl;

				break;


			case 4:
				cout << "Thank You" << endl;
				break;





			}
		
	}
	else {
		cout << "Wrong password Try Again" << endl;
		cin >> password;
	}
	
} while (choice <4);



}



int main()
{
show();

process();
	





	return 0;
}


