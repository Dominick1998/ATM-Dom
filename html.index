/*
Quest 2
Dominick Ferro
Programming 2
Alexander Jaeger
March 19, 2020
*/

/*
I was having trouble 
transfering from one account to another 
so I decided to just create a desposit 
and a withdrawal option(Sorry!)
*/


#include <iostream>  
#include <cstdlib>    
#include <cmath>      

using namespace std;  

void main_menu();

int main () {
//starting checkings balance($1000)
         double check = 1000, 
//starting savings balance($500)
                save = 500,      
//withdrawal amount
                withdraw,   
//deposit amount
                deposit; 
//menu selection
         int option = 0,  
//Input PIN number
               PIN = 0,     
//deposit or withdrawal selection
               selection = 0;    

cout << "Authorization\n";      
//four attempts allowed
  for(int i =0; (PIN != 1998); ++i){    
    if (i == 4){
      cout <<  "Too many wrong attempts!\n";
      return EXIT_SUCCESS;
    }
    cout << "Please Enter 4 Digit PIN(1998)\n> ";
//Gets PIN
    cin >> PIN;                 

}

//main menu system
   main_menu();                 

//navigates through menu
  while(option != 4){  
//4 exits program
    cout << "> ";               
     cin >> option;
   switch(option){
//withdrawal menu
case 1:
        cout << "Choose Account You Wish To\n"
       << "Make A Withdrawal.\n"
       << "[1]  Checking\n"   
       << "[2]  Savings\n"
       << "[3]  Cancel\n> ";
       
//gets menu selection
  cin >> selection;         
  
//navigates through menu
    switch(selection){ 
        
//checking withdrawal
      case 1:        
      
        cout << "{WITHDRAW}\n"
             << "Must Be A Multiple Of $10\n>";
//show amount
         cin >> withdraw;       
        while(fmod(withdraw,10.00)!=0){
          cout << "Not A Multiple Of $10 Try Again\n> ";
           cin >> withdraw;
        }
        
//overdraft protection
        if(withdraw > check){  
          cout << "Insufficient funds in account to\n"
               << "Withdraw Cash" << withdraw << endl << endl;
        }else{
 //shows new balance
        check -= withdraw;     
        }
        break;
        
//savings withdrawal
      case 2:
      
          cout << "{WITHDRAW}\n";
          cout << "Must be a multiple Of $10\n> ";
//gets amount, checks for mult of 10
           cin >> withdraw;      
        while(fmod(withdraw,10.00)!=0){
          cout << "Not A Multiple Of $10 Try Again\n> ";
           cin >> withdraw;
        }
//no overdraw
        if(withdraw > save){      
          cout << "Insufficient funds in the account\n"
        << "withdraw $" << withdraw << endl << endl;
        }else{
//shows new balance
        save -= withdraw;     
        }
        break;
        
//exits withdrawal menu
      case 3:         
      
        break;
//allows more than one attempt
      default:              
        cout << "Invalid choice " << selection
             << " Try Again\n";
        cout << "Choose Account You Wish To\n"
             << "Make A Withdrawal\n"
             << "[1]  Checking\n"
             << "[2]  Savings\n"
             << "[3]  Cancel\n> ";
        cin >> selection;

        break;
}             

//deposit menu
case 2:

  cout << "Choose the account to\n"
       << "make a Deposit\n"
       << "{1}  Checking\n"   
       << "{2}  Savings\n"
       << "{3}  Cancel\n> ";
//gets menu selection
   cin >> selection;          

//navigates through menu
    switch(selection){ 
        
//checking deposit
      case 1:    
      
        cout << "{DEPOSIT}\n";
         cin >> deposit;
       check += deposit;  
//calculates new balance
        break;
        
//savings deposit
      case 2:  
      
        cout << "{DEPOSIT}\n> ";
         cin >> deposit;
        save += deposit;     
//calculates new balance
        break;
        
//exits menu
      case 3:     
      
        break;
      default:      
//allows more than one attempt
        cout << "Invalid choice " << selection
             << " Try Again\n";
        cout << "Choose The Account You Wish To\n"
             << "Make A Withdrawal\n"
             << "{1}  Checking\n"
             << "{2}  Savings\n"
             << "{3}  Cancel\n> ";
         cin >> selection;
         break;
}
//shows checking and savings balance
case 3:
        cout << "Checking Balance: $" << check << endl;
        cout << "Savings Balance: $" << save << endl << endl;

 //let them make another choice
  main_menu();      
        break;
        
//exits
case 4:       

        break;
      default:       
//allows retries
        cout << option << " Not a valid "
             << "option, please try again\n";
    }
  }
  return EXIT_SUCCESS;
}

/*MAIN-MENU-LAYOUT*/

void main_menu(){            
  cout << "Please Select An Option\n"
       << "{1}  Withdrawal\n"
       << "{2}  Deposit\n"
       << "{3}  Display Balances\n"
       << "{4}  Termination of program(quit)\n";
  cout << "{5}  Logout\n";
}

//end of code
