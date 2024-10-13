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


