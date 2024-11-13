# MY-PROJECT
Microfinance Database: The Loan Wizard
**OVERVIEW**
Built using HTML, CSS, and JavaScript for the frontend, with a Node.js and MySQL backend, Loan wizard offers a seamless user experience 
while ensuring secure and efficient management of loan services.

**Users Table**

UserID (Primary Key)
Name
Address
Contact Information (Phone, Email)
Loan Eligibility Status

**Loan Amounts Table**
LoanID (Primary Key)
UserID (Foreign Key)
Loan Amount
Loan Type (e.g., Short-Term, Long-Term)
Loan Purpose

**Interest Rates Table**
InterestRateID (Primary Key)
InterestRate
Loan Type (Foreign Key)

**Repayment Schedules Table**
RepaymentScheduleID (Primary Key)
LoanID (Foreign Key)
Repayment Date
Amount Due

**Transaction Histories Table**
TransactionHistoryID (Primary Key)
LoanID (Foreign Key)
Transaction Date
Transaction Type (e.g., Loan Disbursement, Repayment)
Transaction Amount
Remaining Balance

**Database Relationships**
**Users and Loan Amounts****: One-to-Many (each user can have multiple loans)
**Loan Amounts and Interest Rates**: Many-to-One (each loan has one interest rate)
**Loan Amounts and Repayment Schedules**: One-to-Many (each loan has one or more repayment schedules)
**Loan Amounts and Transaction Histories**: One-to-Many (each loan can have multiple transactions)


**Data Flow**
When a loan is approved, a new record is created in the Loan Amounts table, and the associated user's information is updated in the Users table.
The interest rate for the loan is determined based on the loan type, and a new record is created in the Interest Rates table.
A repayment schedule is generated for the loan, and new records are created in the Repayment Schedules table.
As payments are made, new records are added to the Transaction Histories table.
The remaining balance on the loan is updated in the Loan Amounts table based on the transaction history.

**Interactivity and User Experience**:
Provide real-time feedback for form submissions (e.g., success messages, error handling).
