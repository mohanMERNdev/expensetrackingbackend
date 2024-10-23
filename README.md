Personal Expense Tracker API
Setup Instructions
Clone the repository to your local machine.

Install the required Node.js packages by running npm install.

Ensure the SQLite database file (expense_tracker.db) is already created and located in the root directory of the project.

Start the server by running npm start.

The API will be accessible at http://localhost:3000 (or a different port if specified by the environment).

API Endpoints
1. Add a Transaction
Method: POST /transactions
Description: Adds a new income or expense transaction.
Request Body (JSON format): You need to provide the type of transaction (income or expense), category, amount, date, and an optional description.
Response: Returns the added transaction with a unique ID.
2. Get All Transactions
Method: GET /transactions
Description: Retrieves all income and expense transactions from the database.
Response: Returns an array of transactions including details like ID, type, category, amount, date, and description.
3. Get a Transaction by ID
Method: GET /transactions/:id
Description: Retrieves a specific transaction by its ID.
Response: Returns the transaction if found, or an error message if the ID is invalid.
4. Update a Transaction by ID
Method: PUT /transactions/:id
Description: Updates an existing transaction by its ID.
Request Body (JSON format): You can update the type, category, amount, date, and description.
Response: Returns the updated transaction details.
5. Delete a Transaction by ID
Method: DELETE /transactions/:id
Description: Deletes a transaction by its ID.
Response: Confirms that the transaction has been deleted.
6. Get Summary
Method: GET /summary
Description: Retrieves a summary of all transactions including total income, total expenses, and balance.
Optional Query Parameters: You can filter the summary by start date, end date, or category.
Response: Returns the total income, total expenses, and balance.
Example Postman Usage
Add a Transaction
Method: POST
URL: http://localhost:3000/transactions
Description: You can add a transaction by sending a POST request with the transaction details like type, category, amount, date, and description.
License
This project is licensed under the MIT License.