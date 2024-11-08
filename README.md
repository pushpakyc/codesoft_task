# codesoft_task1
//Develop a calculator program that performs basic arithmetic operations such as addition, subtraction, multiplication, and division. Allow the user to input two numbers and choose an operation to perform.//
#include <iostream>
#include <limits>  

using namespace std;

int main() {
    double num1, num2;   
    char operation;      
    double result;       

    
    cout << "Welcome to the basic calculator program!" << endl;
    cout << "You can perform the following operations:" << endl;
    cout << "Addition (+), Subtraction (-), Multiplication (*), Division (/)" << endl;


    cout << "Enter the first number: ";
    while (!(cin >> num1)) {
        
        cout << "Invalid input. Please enter a valid number: ";
        cin.clear();  
        cin.ignore(numeric_limits<streamsize>::max(), '\n');  
    }

    cout << "Enter the second number: ";
    while (!(cin >> num2)) {
        cout << "Invalid input. Please enter a valid number: ";
        cin.clear();  
        cin.ignore(numeric_limits<streamsize>::max(), '\n');  
    }

    cout << "Enter the operation (+, -, *, /): ";
    cin >> operation;

    switch (operation) {
        case '+':
            result = num1 + num2;
            cout << "Result: " << num1 << " + " << num2 << " = " << result << endl;
            break;
        case '-':
            result = num1 - num2;
            cout << "Result: " << num1 << " - " << num2 << " = " << result << endl;
            break;
        case '*':
            result = num1 * num2;
            cout << "Result: " << num1 << " * " << num2 << " = " << result << endl;
            break;
        case '/':
            if (num2 != 0) {
                result = num1 / num2;
                cout << "Result: " << num1 << " / " << num2 << " = " << result << endl;
            } else {
                cout << "Error: Division by zero is not allowed." << endl;
            }
            break;
        default:
            cout << "Invalid operation. Please select one of (+, -, *, /)." << endl;
            break;
    }

    return 0;
}
