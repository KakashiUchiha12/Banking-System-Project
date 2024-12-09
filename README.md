# 💻 Project Documentation: JavaFX Banking Application 🏦

---

## 🌟 Project Overview
The **JavaFX Banking Application** is a desktop-based banking management system built using JavaFX, offering an interactive and intuitive interface for performing essential banking tasks. The system supports user and admin roles with specific functionalities tailored for each.

---

## 🎯 Purpose of the Application
The main purpose of this project is to simulate a banking system where users can manage their accounts, while administrators can handle account-related operations. Key features include account management, secure login, deposits, withdrawals, fund transfers, and transaction history.

### **Target Audience:**
- **Regular Users**: Access personal account features like balance check, deposits, withdrawals, and transfers.
- **Admin Users**: Manage all user accounts, add/remove users, and view account details.

---

## 🛠️ Key Features
### **1. User Dashboard 🧑‍💻**:
   - **Login**: Secure login via username and password.
   - **Account Management**: Deposit, withdraw, and transfer funds.
   - **Account Details**: View account holder’s name, account number, and current balance.
   - **Transaction History**: Display a list of transactions.
   - **Logout**: Securely logout from the system.

### **2. Admin Dashboard 👨‍💼**:
   - **Login**: Admins can log in using admin credentials.
   - **Account Search**: Admin can search user accounts by account number or holder name.
   - **Account Creation**: Admin can add new bank accounts.
   - **Account Removal**: Admin can delete accounts.
   - **Account Overview**: View all user accounts with details.

### **3. Authentication 🔐**:
   - Secure login system to ensure only authorized access for both users and admins.
   - Admin login uses specific admin credentials.

---

## 🔧 Technologies Used
- **JavaFX**: For creating the GUI with FXML.
- **FXML**: To design the UI components in a declarative style.
- **Java**: Core programming language for the backend logic and application flow.
- **CSV Files**: Used for storing user data (account details) persistently.

---

## 📚 System Architecture
The application uses the **Model-View-Controller (MVC)** architecture:
1. **Model**: Represents the data (bank accounts, user credentials).
2. **View**: The graphical interface of the application designed using FXML.
3. **Controller**: Manages user interactions, updates the model, and updates the view accordingly.

---

## 📂 Class and Functionality Breakdown

### **1. MainApp (Java Class)**
   - **Role**: Entry point of the application. Initializes the stage (window) and loads the login screen.
   - **Responsibilities**:
     - Setting up window size, title, and login screen.
     - Ensures proper navigation for different screens (User Dashboard, Admin Dashboard).

### **2. Navigation (Utility Class)**
   - **Role**: Simplifies scene navigation.
   - **Responsibilities**:
     - Handles scene transitions between login, user dashboard, and admin dashboard.

### **3. AccountDatabase (Utility Class)**
   - **Role**: Manages loading and saving of account data.
   - **Responsibilities**:
     - Loads and saves user data from/to a CSV file.
     - Supports account search, addition, and removal.

### **4. BankAccount (Model Class)**
   - **Role**: Represents a bank account.
   - **Responsibilities**:
     - Stores account-related information such as account number, holder’s name, and balance.

### **5. UserAccount (Model Class)**
   - **Role**: Represents user credentials.
   - **Responsibilities**:
     - Stores user login details (username, password) and balance.

### **6. AdminDashboardController (Controller Class)**
   - **Role**: Manages the admin dashboard.
   - **Responsibilities**:
     - Handles actions like account creation, removal, and account search.

### **7. UserDashboardController (Controller Class)**
   - **Role**: Manages the user dashboard.
   - **Responsibilities**:
     - Handles actions such as deposit, withdrawal, transfer, and viewing transaction history.

### **8. LoginController (Controller Class)**
   - **Role**: Handles user authentication.
   - **Responsibilities**:
     - Validates username and password for both users and admins.

---

## 👥 User Flow
### **1. Login**
   - User/Admin enters username and password.
   - If credentials are valid, they are redirected to the appropriate dashboard (User/Admin).

### **2. User Dashboard**
   - User can view account balance, perform transactions, and view transaction history.

### **3. Admin Dashboard**
   - Admin can search for accounts, create new accounts, remove existing accounts, and view all accounts in the system.

### **4. Logout**
   - The user or admin can log out and return to the login screen.

---

## 💾 Data Persistence
The application uses **CSV files** for storing user and account information:
- **Accounts.csv**: Stores account details (account number, holder’s name, balance).
- **User Credentials**: Used for user login authentication.

---

## 🔒 Security Considerations
- **Password Security**: Currently, passwords are stored in plain text. In real applications, it is recommended to hash passwords using a secure algorithm like bcrypt.
- **File Integrity**: Data is stored in CSV files, which can be manually altered. In production, a relational database with proper security should be used.
- **User Input Validation**: Basic validation is implemented, but more advanced validation (e.g., format checks) could be added for robustness.

---

## 🚀 Possible Improvements
1. **🔐 Enhanced Password Security**:
   - Implement password hashing (bcrypt or PBKDF2) to ensure better security for user credentials.
   
2. **💾 Database Integration**:
   - Move from CSV file storage to a relational database (MySQL, PostgreSQL) for better scalability, data integrity, and security.
   
3. **📅 Transaction Date and Time**:
   - Add timestamps for each transaction to maintain a record of when deposits, withdrawals, and transfers took place.

4. **🌐 Multi-User Support**:
   - Enable concurrent access for multiple users (e.g., multiple admins or users logged in at the same time).
   
5. **📱 Mobile App Integration**:
   - Consider building a mobile version of the application (Android/iOS) for users who want to access their accounts on the go.

6. **📊 Analytics and Reports**:
   - Add features for generating reports on transaction history, account balances, and other financial metrics.

7. **🛡️ Improved Error Handling**:
   - Add more robust error handling, especially for edge cases (e.g., invalid inputs, insufficient funds).
   
8. **💬 User Feedback**:
   - Allow users to provide feedback or comments about their banking experience.

---

## 🎉 Conclusion
The **JavaFX Banking Application** is a functional and secure desktop application for basic banking tasks. While it provides essential features such as account management, deposits, withdrawals, and transaction history, it can be further improved with better security, database integration, and additional features. With these enhancements, the application could be transformed into a robust and scalable banking solution for real-world use.
