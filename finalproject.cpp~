/* 
 * Author: Joel Smith
 * Date Created: May 20, 2014, 2:00 PM
 * Last Modification Date: June 8, 2014 4:00 PM
 * File name:   finalproject.cpp
 *
 * Overview:
 *	This program is a business simulation game.
 *	
 * Input:
 *	This program inputs interger menu choices for the player to choose their action
 *
 *	Example input:
 *	1, 4
 *
 * Output:
 *	This program outputs strings denoting actions taken by player and current player status
 *	
 *	
 *	
 *
 *
 *
 *******************************************************************************/ 


#include <iostream>
#include <string>
#include <ctime>
#include <stdlib.h>
#include <time.h>


using namespace std;

void inputCheckInterger(int &input);



int randomInt(int min, int max);


//REQUIREMENT 20
struct businessTypes
{

string business1;

string business2;

string business3;

};

//END REQUIREMENT 20

class business
{
	
	public:

	int cost;
	
//REQUIREMENT 17
	
//REQUIREMENT 22
	
	int businessEaseOfUse[3][3];
	
	int *p3;



//END REQUIREMENT 22	
	
//END REQUIREMENT 17	
	
	string className;

	int incomeCeiling;

	int incomeFloor;
	
//REQUIREMENT 15

	string status;	

//END REQUIREMENT 15
};	

//REQUIREMENT 21
class player
{

	public:

	string name;

	int money;

	int numberOfBusinessesOwned;

	//business businessesOwned[100];

	//REQUIREMENT 18
	
	business* businessesOwned[100];
	
	//END REQUIREMENT 18
	
	/*

	business* businessesOwned;

	businessesOwned = new business[];	

	*/

	void displayCurrentMoney();

	void buyBusiness(int classNumber);

	void sellBusiness();

	void displayBusinessesOwned();

	private:

};
//END REQUIREMENT 21



class businessIcecreamshop : public business
{

	public:

	businessIcecreamshop();

	

};

class businessRestaurant : public business
{

	public:

	businessRestaurant();
	

};

class businessGym : public business
{

	public:

	businessGym();

	
};

class timeClass
{
	public:
	
	void nextTurn(player& player1); //This function executes the next turn 
	

};

class menu
{

	public:

	void displayMenuMain();

	void displayBuyOptions();

	

};

int main(int argc, char *argv[])
{

	
	int p4;
	
	int p5;

	timeClass timeObj;

	menu menu1;

	int money;

	player player1;

	player1.numberOfBusinessesOwned = 0;

	int  menuChoice;

	//REQUIREMENT 1
	cout << "Business simulation text game." << endl << endl << endl;

	//END REQUIREMENT 1

	//REQUIREMENT 2

	//REQUIREMENT 3
	
	//REQUIREMENT 19

	//cout << "Argc is: " << argc << endl;
	
	if (argc != 2)
	{
	
		cout << "Player: Enter the amount of starting money:  " << endl;

		cin >> money;
		
	}
	
	else if (argc == 2)
	{
	
		money = atoi(argv[1]);
	
		//POINTERX	
	}	
	
	//END REQUIREMENT 19
	
	inputCheckInterger(money);

	player1.money = (int)(money);

	cout << endl << endl;


	

	//END REQUIREMENT 2

	
	//END REQUIREMENT 3

	menuChoice = 0;

	//REQUIREMENT 4
	
	//REQUIREMENT 5

	//REQUIREMENT 6

	while (menuChoice != 5)

	{

		menu1.displayMenuMain();
		
		
		
		player1.displayCurrentMoney();

		cout << "Please make a menu choice: " << endl;

		cin >> menuChoice;



//REQUIREMENT 9

//cout menuChoice

//This debugging trick is uncommented to show that the right type of value is in the variable

//END REQUIREMENT 9

		
		inputCheckInterger(menuChoice);

		cout << endl << endl;

		if (menuChoice == 1)
		{

			menu1.displayBuyOptions();

			int buyChoice = 0;

			cout << "Enter the number of the business to buy: ";

			cin >> buyChoice;
			
			inputCheckInterger(buyChoice);

			cout << endl << endl;

			while (buyChoice < 1 || buyChoice > 4)
			{
				cout << "Buy choice is invalid. Must be interger beweetn 1 and 4: " << endl;

			}

			if (buyChoice == 1)
			{

			player1.buyBusiness(buyChoice);

			}

			else if (buyChoice == 2)
			{

			player1.buyBusiness(buyChoice);

			}

			else if (buyChoice == 3)
			{

			player1.buyBusiness(buyChoice);

			}

			else if (buyChoice == 4)
			{

			

			}
			

		}

		else if (menuChoice == 2)
		{

		player1.sellBusiness();

		}

		else if (menuChoice == 3)
		{


		player1.displayBusinessesOwned();

		}

		else if (menuChoice == 4)
		{
		
		timeObj.nextTurn(player1);

		}

	}

	//END REQUIREMENT 4
	
	//END REQUIREMENT 5

	//END REQUIREMENT 6

}

void menu::displayMenuMain()
{

	cout << "1: Buy business." << endl;

	cout << "2: Sell business." << endl;

	cout << "3: Display list of currently owned businesses." << endl;

	cout << "4: End turn." << endl;

	cout << "5: Quit game." << endl << endl;

}

void menu::displayBuyOptions()
{

	cout << "Businesses available to buy are: " << endl << endl;

	cout << " 1: Ice Cream Shop. " << endl;
	cout << "	cost: 20000" << endl;
	cout << "	income ceiling: 5000" << endl;
	cout << "	income floor: 1000" << endl << endl;


	cout << " 2: Restaurant. " << endl;
	cout << "	cost: 100000" << endl;
	cout << " 	income ceiling: 40000"; 
	cout << "	income floor: 3000" << endl << endl;

	cout << " 3: Gym. " << endl;
	cout << "	cost 1000000" << endl;
	cout << "	income ceiling: 600000" << endl;
	cout << "	income floor: 200000" << endl << endl;

	cout << " 4: Back to menu." << endl << endl;
}

void player::displayBusinessesOwned()
{

	//cout << "You currently own " << this->numberOfBusinessesOwned << " businesses: " << endl << endl;


	for (int i = 0; i < this->numberOfBusinessesOwned; i++) 
	{

	if (this->businessesOwned[i]->status == "bought")
	{

		cout << "At index: " << i << " ";
		cout << this->businessesOwned[i]->className; 
		cout << endl;
		cout << "Income ceiling for this business is: " << this->businessesOwned[i]->incomeCeiling <<  " .";
		cout << " Income floor for this business is: " << this->businessesOwned[i]->incomeFloor;
		cout << endl << endl;

	}
	}

}

//REQUIREMENT 8
/*

if the next class was defined incorrectly such as businessIcecreamshop:businessIcecreamshop(){} then it would be a syntax error

if the wrong amount of value for a variable was input then it would be a logic error, as the wrong logic is used in the program

if a non int value was input into the class variables then it would be a runtime error as it would be input at runtime


*/

businessIcecreamshop::businessIcecreamshop()
{

	this->className = "Ice Cream Shop";

	this->cost = 20000;

	this->incomeCeiling = 5000;

	this->incomeFloor = 1000; 

}

businessRestaurant::businessRestaurant()
{

	this->className = "Restaurant";

	this->cost = 100000;

	this->incomeCeiling = 40000;

	this->incomeFloor = 3000;




}

businessGym::businessGym()
{

	this->className = "Gym";

	this->cost = 1000000;

	this->incomeCeiling = 600000;

	this->incomeFloor = 200000;

}

void player::displayCurrentMoney()
{

	cout << "Player's current money balance is: $" << this->money << endl;

}

void player::buyBusiness(int classNumber)
{

	for (int i = 0; i <= this->numberOfBusinessesOwned; i++)
	{

		if (i == numberOfBusinessesOwned)	
		{

			if (classNumber == 1)
			{

				if (this->money >= 20000)
				{ 

				
				
					this->businessesOwned[i] = new businessIcecreamshop;

					this->businessesOwned[i]->status = "bought";
					
					this->numberOfBusinessesOwned++;

					this->money = this->money - 20000;

					break;

				}

				else
				{

					cout << "You do not have enough money to purchase this type of business." << endl << endl;

				}
				
				

			}

			else if (classNumber == 2)
			{

				if (this->money >= 100000)
				{

					this->businessesOwned[i] = new businessRestaurant;

					this->businessesOwned[i]->status = "bought";
	
					this->numberOfBusinessesOwned++;

					this->money = this->money - 100000;
					
					break;

				}

				else
				{

					cout << "You do not have enough money to purchase this type of business." << endl << endl;

				}

			}

			else if (classNumber == 3)
			{

				if (this->money >= 1000000)
				{


					this->businessesOwned[i] = new businessGym;

					this->businessesOwned[i]->status = "bought";

					this->numberOfBusinessesOwned++;

					this->money = this->money - 1000000;
				
					break;

				}

				else
				{

					cout << "You do not have enough money to purchase this type of business." << endl << endl;

				}
				

				
				
				


			}
		
		

		}
	
	}

	

}

void player::sellBusiness()
{


//REQUIREMENT 12
//variable indexToSell is only available within this code block

	int indexToSell;

//END REQUIREMENT 12
	
	
	cout << "Player: Enter the index for the business to sell: ";

	cin >> indexToSell;
	
	inputCheckInterger(indexToSell);

	if (businessesOwned[indexToSell]->status == "bought")
	{

		this->money = this->money + businessesOwned[indexToSell]->cost;

	

		businessesOwned[indexToSell]->status = "sold";
	}

	else if(businessesOwned[indexToSell]->status == "sold")
	{

		cout << "This business cannot be sold because it was already sold" << endl << endl;

	}

	else if(businessesOwned[indexToSell] == NULL)
	{

		cout << "You do not own a business at this index." << endl << endl;

	}

}

void timeClass::nextTurn(player& player1)
{



	int incomeThisTurn = 0;

	for (int i = 0; i < player1.numberOfBusinessesOwned; i++)
	{

//REQUIREMENT 7	
	
		if (player1.businessesOwned[i]->className == "Ice Cream Shop" && player1.businessesOwned[i]->status == "bought")
		{

			incomeThisTurn = incomeThisTurn + randomInt(player1.businessesOwned[i]->incomeFloor, player1.businessesOwned[i]->incomeCeiling);

		}

//END REQUIREMENT 7		
		
		else if (player1.businessesOwned[i]->className == "Restaurant" && player1.businessesOwned[i]->status == "bought")
		{

			incomeThisTurn = incomeThisTurn + randomInt(player1.businessesOwned[i]->incomeFloor, player1.businessesOwned[i]->incomeCeiling);

		}

		else if (player1.businessesOwned[i]->className == "Gym" && player1.businessesOwned[i]->status == "bought")
		{

			incomeThisTurn = incomeThisTurn + randomInt(player1.businessesOwned[i]->incomeFloor, player1.businessesOwned[i]->incomeCeiling);
		
		}

	}

	player1.money = player1.money + incomeThisTurn; 
	
}


int randomInt(int min, int max)
{
srand(time(NULL));

return (rand() % (max - min) + min);
}	


//REQUIREMENT 10	

//REQUIREMENT 11

void inputCheckInterger(int &input)

//END REQUIREMENT 10

//END REQUIREMENT 11

//REQUIREMENT 14

{

	while(cin.fail())
	{
		cout << "Invalid input. Must be interger.";
	
		cin.clear();
	
		cin.ignore(9999, '\n');
	
		cout << " Enter again: " << endl;
	
		cin >> input;
	}

}

int count = 0;

void recourseWelcome(int times)
{

	count++;

	cout << "Welcome to the business simulation text game!";
	
	if (count == times)
	{
	
		return;
	
	}
	
	else
	{
	
		recourseWelcome(times);
	
	}
	
	

}

void inputCheckInterger(string &input)
{

	while(cin.fail())
	{
	
		cout << "Invalid input. Must be std::string type. ";
		
		cin.clear();
		
		cin.ignore(9999, '\n');
		
		cout << " Enter again: " << endl;
		
		cin >> input;
		
	}
	
}

//END REQUIREMENT 14
	
	
	


	
	
	
	
	
	
