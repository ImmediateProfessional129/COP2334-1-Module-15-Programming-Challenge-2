# COP2334-1-Module-15-Programming-Challenge-2
This is a repository link of the COP2334-1 Module 15 Programming Challenge 2

// PreferredCustomer Class

// This program is designed to produce the customer's information and display the discount percentage. Plus, their names, addresses, phone numbers, purchase amount, and customer number.

#include <iostream> // Header file for input and output
#include <string> // Header file for strings
using namespace std; // Standard namespace

class CustomerData; // Class declaration
class PreferredCustomer; // Class declaration

class CustomerData { // Class definition
private: // Private members
  string lastName; // Last name
  string firstName; // First name
  string address; // Address
  string city; // City
  string state; // State
  string zip; // Zip
  string phone; // Phone number
  string customerNumber; // Customer number
  bool mailingList; // Mailing list
public: // Public members
  CustomerData(); // Default constructor
  CustomerData(string, string, string, string, string, string, string, string, bool, string, string, string, string, string, string); // Constructor with parameters
  void setLastName(string); // Setter for last name
  void setFirstName(string); // Setter for first name
  void setAddress(string); // Setter for address
  void setCity(string); // Setter for city
  void setState(string); // Setter for state
  void setZip(string); // Setter for zip
  void setPhone(string); // Setter for phone
  void setCustomerNumber(string); // Setter for customer number
  void setMailingList(bool); // Setter for mailing list
  string getLastName(); // Getter for last name
  string getFirstName(); // Getter for first name
  string getAddress(); // Getter for address
  string getCity(); // Getter for city
  string getState(); // Getter for state
  string getZip(); // Getter for zip
  string getPhone(); // Getter for phone
  string getCustomerNumber(); // Getter for customer number
  bool getMailingList(); // Getter for mailing list
};

class PreferredCustomer : public CustomerData { // Class definition
private: // Private members
  double purchasesAmount; // Purchases amount
  double discountLevel; // Discount level
public: // Public members
  PreferredCustomer(); // Default constructor
  PreferredCustomer(string, string, string, string, string, string, string, string, bool, string, string, string, string, string, string, double, double); // Constructor with parameters
  void setPurchasesAmount(double); // Setter for purchases amount
  void setDiscountLevel(double); // Setter for discount level
  double getPurchasesAmount(); // Getter for purchases amount
  double getDiscountLevel(); 
};

CustomerData::CustomerData() { // Default constructor
  lastName = ""; // Last name
  firstName = ""; // First name
  address = ""; // Address
  city = ""; // City
  state = ""; // State
  zip = ""; // Zip
  phone = ""; // Phone number
  customerNumber = ""; // Customer number
  mailingList = false; // Mailing list
}

CustomerData::CustomerData(string l, string f, string a, string c, string s, string z, string p, string cn, bool ml, string ln, string fn, string ad, string cy, string st, string zp) { // Constructor with parameters
  lastName = l; // Last name
  firstName = f; // First name
  address = a; // Address
  city = c; // City
  state = s; // State
  zip = z; // Zip
  phone = p; // Phone number
  customerNumber = cn; // Customer number
  mailingList = ml; // Mailing list
} 

void CustomerData::setLastName(string l) { // Setter for last name
  lastName = l; // Last name
} 
void CustomerData::setFirstName(string f) { // Setter for first name
  firstName = f; // First name
} 
void CustomerData::setAddress(string a) { // Setter for address
  address = a; // Address
} 
void CustomerData::setCity(string c) { // Setter for city
  city = c; // City
} 
void CustomerData::setState(string s) { // Setter for state
  state = s; // State
} 
void CustomerData::setZip(string z) { // Setter for zip
  zip = z; // Zip
} 
void CustomerData::setPhone(string p) { // Setter for phone
  phone = p; // Phone
} 
void CustomerData::setCustomerNumber(string cn) { // Setter for customer number
  customerNumber = cn; // Customer number
} 
void CustomerData::setMailingList(bool ml) { // Setter for mailing list
  mailingList = ml; // Mailing list
} 
string CustomerData::getLastName() { // Getter for last name
  return lastName; // Return last name
} 
string CustomerData::getFirstName() { // Getter for first name
  return firstName; // Return first name
}
string CustomerData::getAddress() { // Getter for address
  return address; // Return address
}
string CustomerData::getCity() { // Getter for city
  return city; // Return city
}
string CustomerData::getState() { // Getter for state
  return state; // Return state
}
string CustomerData::getZip() { // Getter for zip
  return zip; // Return zip
}
string CustomerData::getPhone() { // Getter for phone
  return phone; // Return phone
}
string CustomerData::getCustomerNumber() { // Getter for customer number
  return customerNumber; // Return customer number
}
bool CustomerData::getMailingList() { // Getter for mailing list
  return mailingList; // Return mailing list
}
PreferredCustomer::PreferredCustomer() { // Default constructor
  purchasesAmount = 0; // Purchases amount
  discountLevel = 0; // Discount level
}
PreferredCustomer::PreferredCustomer(string l, string f, string a, string c, string s, string z, string p, string cn, bool ml, string ln, string fn, string ad, string cy, string st, string zp, double pa, double dl) : CustomerData(l, f, a, c, s, z, p, cn, ml, ln, fn, ad, cy, st, zp) { // Constructor with parameters
  purchasesAmount = pa; // Purchases amount
  discountLevel = dl; // Discount level
}
void PreferredCustomer::setPurchasesAmount(double pa) { // Setter for purchases amount
  purchasesAmount = pa; // Purchases amount
}
void PreferredCustomer::setDiscountLevel(double dl) { // Setter for discount level
  discountLevel = dl; // Discount level
}
double PreferredCustomer::getPurchasesAmount() { // Getter for purchases amount
  return purchasesAmount; // Return purchases amount
}
double PreferredCustomer::getDiscountLevel() { // Getter for discount level
  return discountLevel; // Return discount level
}

int main() { // Main function
  PreferredCustomer customer1("Washington", "Alex", "243 AntHill St", "Los Angeles", "CA", "25476", "213-646-2169", "64913", true, "Washington", "Alex", "243 AntHill St", "Los Angeles", "CA", "25476", 1000, 0.05); // Customer 1
  cout << "Customer 1: " << endl; // Output for the customer
  cout << "Last Name: " << customer1.getLastName() << endl; // Output for the last name
  cout << "First Name: " << customer1.getFirstName() << endl; // Output for the first name
  cout << "Address: " << customer1.getAddress() << endl; // Output for the address
  cout << "City: " << customer1.getCity() << endl; // Output for the city
  cout << "State: " << customer1.getState() << endl; // Output for the state
  cout << "Zip: " << customer1.getZip() << endl; // Output for the zip
  cout << "Telephone Number: " << customer1.getPhone() << endl; // Output for the telephone number
  cout << "Customer Number: " << customer1.getCustomerNumber() << endl; // Output for the customer number
  cout << "Mailing List: " << customer1.getMailingList() << endl; // Output for the mailing list
  cout << "Purchases Amount: " << customer1.getPurchasesAmount() << endl; // Output for the purchases amount
  cout << "Discount Level: " << customer1.getDiscountLevel() << endl; // Output for the discount level
  cout << endl; // New line
  PreferredCustomer customer2("Deerfield", "Jacob", "456 Elm St", "Springfield", "OH", "54321", "216-783-9261", "93614", true, "Deerfield", "Jacob", "456 Elm St", "Springfield", "OH", "54321", 15000, 0.30); // Customer 2
  cout << "Customer 2: " << endl; // Output for the customer
  cout << "Last Name: " << customer2.getLastName() << endl; // Output for the last name
  cout << "First Name: " << customer2.getFirstName() << endl; // Output for the first name
  cout << "Address: " << customer2.getAddress() << endl; // Output for the address
  cout << "City: " << customer2.getCity() << endl; // Output for the city
  cout << "State: " << customer2.getState() << endl; // Output for the state
  cout << "Zip: " << customer2.getZip() << endl; // Output for the zip
  cout << "Telephone Number: " << customer2.getPhone() << endl; // Output for the telephone number
  cout << "Customer Number: " << customer2.getCustomerNumber() << endl; // Output for the customer number
  cout << "Mailing List: " << customer2.getMailingList() << endl; // Output for the mailing list
  cout << "Purchases Amount: " << customer2.getPurchasesAmount() << endl; // Output for the purchases amount
  cout << "Discount Level: " << customer2.getDiscountLevel() << endl; // Output for the discount level
  cout << endl; // New line
  PreferredCustomer customer3("Hartford", "Chris", "341 Sugarcoat St", "Houston", "TX", "28347", "281-537-9153", "72916", true, "Hartford", "Chris", "341 Sugarcoat St", "Houston", "TX", "28347", 1800, 0.09); // Customer 3
  cout << "Customer 3: " << endl; // Output for the customer
  cout << "Last Name: " << customer3.getLastName() << endl; // Output for the last name
  cout << "First Name: " << customer3.getFirstName() << endl; // Output for the first name
  cout << "Address: " << customer3.getAddress() << endl; // Output for the address
  cout << "City: " << customer3.getCity() << endl; // Output for the city
  cout << "State: " << customer3.getState() << endl; // Output for the state
  cout << "Zip: " << customer3.getZip() << endl; // Output for the zip
  cout << "Telephone Number: " << customer3.getPhone() << endl; // Output for the telephone number
  cout << "Customer Number: " << customer3.getCustomerNumber() << endl; // Output for the customer number
  cout << "Mailing List: " << customer3.getMailingList() << endl; // Output for the mailing list
  cout << "Purchases Amount: " << customer3.getPurchasesAmount() << endl; // Output for the purchases amount
  cout << "Discount Level: " << customer3.getDiscountLevel() << endl; // Output for the discount level
  cout << endl; // New line
  return 0; // Return 0
}
