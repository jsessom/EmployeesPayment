# EmployeesPayment
Calculating the Rate of Pay for your Employees.
#include <iostream>
#include <math.h>
#include <iomanip>
#include <string>

using namespace std;
int main()

{
	double  rateperhour, grosssalary, netsalary, tax;
	int weeklyhours, employees, LCV, size;

	cout << " Please enter the number of loops you wish to perform. " << endl;
	cin >> size;

	for (LCV = 0; LCV < size; LCV++)
	{

		cout << " Please enter the number of weekly hours for your employee. " << endl;
		cin >> weeklyhours;

		cout << " Please enter the rate per hour for your employee. " << endl;
		cin >> rateperhour;

		grosssalary = weeklyhours * rateperhour;

		if (grosssalary > 2200.00)
		{
			tax = .28 * grosssalary;
			netsalary = grosssalary - tax;

		}
		else
		{
			tax = .21 * grosssalary;
			netsalary = grosssalary - tax;
		}
		cout << "The weekly hours for your employee is " << weeklyhours << setw(3)<<left<< endl;
		cout << "The rate per hour for your employee is " << rateperhour << setw(3) << left<< endl;
		cout << "The tax is " << tax << setw(3) << left<< endl;
		cout << "The net salary for your employee = " << netsalary << setw(3) << left<< endl;
		cout << endl;

		}

	system("pause ");
	return 0;

}
