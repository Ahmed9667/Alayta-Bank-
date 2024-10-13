# Alayta-Bank-
Alayta Bank, a microfinance institution, faced challenges
due to a heavily denormalized dataset, leading to
inefficiencies in data storage, high redundancy, and
performance issues.This case study outlines the process
of normalizing the dataset from its initial denormalized
form to the Third Normal Form (3NF). The primary goal
is to enhance data integrity, reduce redundancy, and
improve the overall efficiency of the database.

## Business Problem Statement
● Alayta Bank's denormalized database includes redundant and repetitive data
across various customer, loan, and payment-related fields. This has caused:
○ Data redundancy: Duplicated information across multiple rows.
○ Anomalies in updates: Modifying one record may lead to inconsistencies
across others.
○ Slower query performance: Due to a larger dataset with repeating values.
○ Data integrity risks: Lack of proper constraints means inaccurate or duplicate
data can easily be entered.
● The goal is to transform this dataset through normalization into a series of
well-structured tables, reducing data redundancy, improving data integrity, and
streamlining query performance.

## Project Scope:

### 1.Convert Denormalized to 1NF:
- Each `ID column` must have unique records
- Create a composite key of `'CustomerID'` , `'LoanID'` to ensure uniqueness


### 2.Convert 1NF to 2NF:
#### Create table in 2NF structure as :
- ustomers Table >> CustomerID(PK), CustomerName
- loans table >> `LoanID(PK)`, `CustomerID(FK)`, LoanAmount, LoanInterestRate, LoanDuration, LoanStartDate,OfficerID(FK)
- officers table >> `OfficerID(PK)`, OfficerName, OfficerPhone, OfficerEmail, `BranchID(FK)`
- branch table >> `BranchID(PK)`, BranchName, BranchAddress
- payments table >> `PaymentID(PK)`, `LoanID(FK)`, PaymentDate, PaymentAmount
- transactions table >>`TransactionID(PK)`, `LoanID(FK)`, TransactionDate, TransactionType


