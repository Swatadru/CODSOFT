Contact Book
The contact book is a GUI application that allows users to add, view manage their contacts. The application uses a SQLite database to store the contact information, including name, job, and email. The main window displays the contacts in a table view, and users can add new contacts by clicking the "Add" button, which opens a dialog window for data entry.

Running the Application
To run the application, navigate to the project directory and execute the rpcontacts.py script.

Adding a Contact
To add a new contact, click the "Add" button in the main window. This will open the Add Contact dialog, where you can enter the contact's name, job, and email. Click "OK" to save the contact, or "Cancel" to discard changes.

Data Model
The data model for the contact book is provided by the ContactsModel class in the model.py module. This class provides the model that manages the data in your contact database.

Adding a Contact to the Database
To add a new contact to the database, you can call the addContact() method of the ContactsModel class. This method takes a list of three strings representing the contact's name, job, and email, respectively. It then adds a new row to the database and populates the corresponding columns with the provided data.

Connecting the Table View with the Data Model
To display the contact data in the main window, you need to connect the table view with the data model. To perform this connection, you need to call .setModel() on the table view object and pass the model as an argument.

Database Connection
The database connection is provided by the createConnection() function in the database.py module. This function creates a new SQLite database and returns a QSqlDatabase object representing the connection.

Creating the Contacts Table
To create the table that will store the contact data, you can call the _createContactsTable() function in the database.py module. This function creates a new table called contacts with columns for the contact's name, job, and email.

Views
The views for the contact book are provided by the Window class in the views.py module. This class provides the main window and the Add Contact dialog.

Main Window
The main window displays the contacts in a table view and provides a button for adding new contacts. The table view is connected to the data model, so any changes to the data will be automatically reflected in the table.

Add Contact Dialog
The Add Contact dialog is a modal dialog that allows users to enter the name, job, and email of a new contact. The dialog contains three line edits and a button box with "OK" and "Cancel" buttons. When the user clicks "OK", the data is validated and, if valid, added to the database. If the data is invalid, an error message is displayed and the dialog remains open.

Data Validation
The AddDialog class in the views.py module provides the accept() method, which is responsible for validating the user input. If any of the fields are empty, an error message is displayed and the data attribute is set to None. If all fields are filled, the data attribute is set to a list of the three strings representing the name, job, and email.
