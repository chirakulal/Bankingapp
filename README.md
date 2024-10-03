# Bankingapp
**Overview**
This is a simple banking application developed using Java and Spring Boot. It provides basic account management functionality, such as adding accounts, depositing and withdrawing money, fetching account details, and deleting accounts.

<h4>**Features**</h4>
**Create an account:** Add a new bank account.
**Get account details:** Retrieve the details of a specific account by its ID.
**Deposit money:** Deposit a specified amount of money into an account.
**Withdraw money:** Withdraw a specified amount of money from an account.
Get all accounts: Fetch a list of all existing accounts.
Delete an account: Remove a specific account by its ID.
Technologies Used
Java: Programming language.
Spring Boot: Framework for building RESTful web services.
Maven: Dependency management.
Spring Data JPA: Data access layer.
H2: In-memory database for development and testing.
Getting Started
Prerequisites
Before you begin, make sure you have the following installed on your machine:

Java 8 or higher
Maven 3.6 or higher
Installation
Clone the repository:

bash
Copy code
git clone https://github.com/yourusername/bankingapp.git
Navigate to the project directory:

bash
Copy code
cd bankingapp
Build the project:

bash
Copy code
mvn clean install
Run the application:

bash
Copy code
mvn spring-boot:run
The application will start on http://localhost:8080.

API Endpoints
1. Add a New Account
Endpoint: POST /api/accounts
Request Body:
json
Copy code
{
  "accountName": "John Doe",
  "balance": 1000
}
Response: Returns the newly created account object with HTTP status 201 CREATED.
2. Get Account by ID
Endpoint: GET /api/accounts/{id}
Response: Returns the account object with the specified ID.
3. Deposit into Account
Endpoint: PUT /api/accounts/{id}/deposit
Request Body:
json
Copy code
{
  "amount": 500
}
Response: Returns the updated account object with the new balance.
4. Withdraw from Account
Endpoint: PUT /api/accounts/{id}/withdraw
Request Body:
json
Copy code
{
  "amount": 200
}
Response: Returns the updated account object with the new balance.
5. Get All Accounts
Endpoint: GET /api/accounts/get
Response: Returns a list of all accounts.
6. Delete an Account
Endpoint: DELETE /api/accounts/{id}
Response: Returns a success message: "Account is deleted successfully."
Running Tests
The project includes unit tests for the AccountService. To run the tests, use the following Maven command:

bash
Copy code
mvn test
Folder Structure
css
Copy code
bankingapp
├── src
│   ├── main
│   │   ├── java
│   │   │   └── org.canara.bankingapp
│   │   │       ├── controller
│   │   │       │   └── AccountController.java
│   │   │       ├── service
│   │   │       │   └── AccountService.java
│   │   │       └── dto
│   │   │           └── Accountdto.java
│   │   └── resources
│   │       └── application.properties
│   └── test
│       └── java
│           └── org.canara.bankingapp
│               └── AccountServiceTest.java
├── pom.xml
└── README.md
Contributing
Contributions are welcome! Feel free to submit a pull request with your changes or enhancements.
