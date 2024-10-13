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

### Conver 2NF to 3NF:
No transitive dependencies are existed and each table is related to its unique primary key so dataset is fully normalized to 3NF

#### The Schema of Database

![Schema](https://github.com/user-attachments/assets/92e1d371-c505-4543-a85d-d44931afc8fb)


## Data Visualization :
Extracting profitable insights by complex subqueries by creating relations among tables in schema 

#### Top 5 customers whoo had loans in Alayta Bank

![image](https://github.com/user-attachments/assets/281fc754-9b62-4e70-83cc-bc78cc7976d9)

#### Lowest 5 customers who had loans in Alayta Bank

![image](https://github.com/user-attachments/assets/0ddec8f5-5fdb-485c-885a-4b536237b067)

#### Top 5 customers who had loans with transaction deals

![image](https://github.com/user-attachments/assets/fb763476-d7b2-475a-8074-606e70848012)

#### Lowest 5 customers who had loans with transaction deals

![image](https://github.com/user-attachments/assets/b88d404c-268a-4e12-873e-ad2253bc644e)

#### Top 5 customers who had loans withhighest payments

![image](https://github.com/user-attachments/assets/dec2629d-2a97-4797-8d46-2355fb5784a1)


#### Top 5 customers who had loans with loweest payments

![image](https://github.com/user-attachments/assets/3f9b7b5a-d313-4421-9326-dc61721f8b65)


#### Top 5 officers who had the highest loans

![image](https://github.com/user-attachments/assets/48823912-ff90-41ea-b38d-6136adc17566)


#### Top 5 officers who had the lowest loans

![image](https://github.com/user-attachments/assets/d9909538-2a4e-49c0-aa5b-745f69a532a1)


#### Top 5 Branches who had the highest loans

![image](https://github.com/user-attachments/assets/95b98634-9a39-483e-9510-cb59e23cab01)


#### Top 5 Branches who recorded the lowest loans

![image](https://github.com/user-attachments/assets/cccc7c96-f968-4e2d-b244-47f02484dfb4)










