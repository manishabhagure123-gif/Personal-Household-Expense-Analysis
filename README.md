# 🏠 Household Expense Management and Analysis Using PostgreSQL

## 📌 1. Project Overview

The Household Expense Management and Analysis project is a SQL-based database management and financial analysis project developed using PostgreSQL.

The project is designed to organize, record, manage, and analyze household expenses over a three-month period: June, July, and August 2026.

Household expenses are divided into different categories and subcategories, such as groceries, utilities, education, transportation, insurance, EMI payments, medical expenses, and personal expenses.

The database stores financial transactions along with their expense date, amount, family member, vendor, payment method, recurring status, payment status, and transaction description.

Using SQL queries, the project analyzes household spending patterns and provides meaningful information about monthly expenses, category-wise expenditure, family member spending, payment methods, recurring expenses, and high-value transactions.

This project demonstrates practical knowledge of PostgreSQL, relational database management, SQL query writing, database relationships, data integrity, and financial data analysis.

---

## 🎯 2. Business Problem Statement

Managing household expenses is an important part of financial planning.

However, when household transactions are recorded manually or maintained in separate records, it becomes difficult to:

- Understand total household expenditure.
- Identify the categories where most of the money is spent.
- Compare expenses between different months.
- Track expenses associated with individual family members.
- Identify recurring financial commitments.
- Monitor different payment methods.
- Identify high-value transactions.
- Understand monthly household spending patterns.

The objective of this project is to develop a structured PostgreSQL database that stores household financial transactions and uses SQL queries to analyze spending information.

The project provides a practical approach to household expense management through relational database design and SQL-based analysis.

---

## 🎯 3. Project Objectives

The main objectives of this project are:

1. To create a relational database for household expense management.

2. To design structured tables for expense categories, subcategories, family members, payment methods, vendors, and expenses.

3. To establish relationships between tables using primary keys and foreign keys.

4. To maintain data integrity using unique constraints and check constraints.

5. To record household expenses for June, July, and August 2026.

6. To analyze total household expenditure for the selected period.

7. To calculate monthly expense totals and transaction counts.

8. To identify category-wise household spending.

9. To analyze expenses associated with different family members.

10. To compare recurring and non-recurring expenses.

11. To analyze expenses according to payment methods.

12. To identify the highest individual expense transactions.

13. To perform monthly category-wise expense analysis.

14. To classify individual transactions according to their expense amount.

15. To develop practical SQL skills through a real-world financial database project.

---

## 🛠️ 4. Tools and Technologies Used

### PostgreSQL

PostgreSQL is used as the relational database management system.

It stores household expense records in structured tables and allows relationships between different financial information.

### SQL

SQL is used to create database tables, insert financial transactions, retrieve information, and perform financial analysis.

### Database Concepts

The project demonstrates:

- Relational Database Management
- Primary Keys
- Foreign Keys
- Unique Constraints
- Check Constraints
- One-to-Many Relationships
- Data Integrity
- Table Relationships

### SQL Analysis Techniques

The project uses:

- SELECT statements
- INSERT statements
- INNER JOIN
- GROUP BY
- ORDER BY
- COUNT()
- SUM()
- CASE statements
- Date functions
- Aggregate functions
- Subqueries

---

## 🗄️ 5. Database Design

The project contains six main relational tables.

### 5.1 expense_categories

This table stores the main household expense categories.

Examples include:

- Groceries
- Utilities
- Bills
- Recharge
- Medicine
- EMI Payments
- Transportation
- Travel
- Insurance
- Education
- Food Outside
- Personal Care
- Hospital
- Online Shopping

**Purpose:**

To organize household expenses into meaningful financial categories.

### 5.2 expense_subcategories

This table stores detailed expense subcategories.

Examples include:

- Kirana
- Credit Card Bills
- Mobile/WiFi Recharge
- Medicine
- EMI/Home Loan
- Petrol
- Insurance Policy
- School/College Fees
- Stationery
- Personal Tuition

**Purpose:**

To provide detailed classification of household transactions.

The subcategory table is connected to the expense category table using a foreign key.

### 5.3 family_members

This table stores family member information.

The project includes the following member classifications:

- Father
- Mother
- Daughter
- Son
- Family Members

**Purpose:**

To identify the family member associated with each household transaction.

### 5.4 payment_methods

This table stores the available payment methods.

The project includes:

- UPI
- Cash
- Credit Card

**Purpose:**

To analyze household expenses according to the payment method used.

### 5.5 vendors

This table stores vendor and merchant information associated with household expenses.

Examples include:

- Grocery vendors
- Banks
- Mobile service providers
- Medical stores
- Petrol pumps
- Schools
- Hospitals
- Travel providers
- Online shopping platforms

**Purpose:**

To maintain vendor information separately and connect transactions with their respective vendors.

### 5.6 expenses

This is the main transaction table of the project.

It stores household expense information, including:

- Expense ID
- Expense date
- Subcategory ID
- Family member ID
- Vendor ID
- Payment method ID
- Expense amount
- Recurring status
- Payment status
- Transaction description

**Purpose:**

To record and analyze household financial transactions.

The expenses table connects with the other tables through foreign key relationships.

---

## 🔗 6. Database Relationships

The database uses relational table structures to organize household financial information.

### Category and Subcategory Relationship

One expense category can contain multiple expense subcategories.

For example:

The EMI Payments category can contain:

- EMI/Home Loan
- Personal Loan
- Mutual Fund

This relationship helps organize detailed expenses under their main categories.

### Subcategory and Expense Relationship

One subcategory can be associated with multiple expense transactions.

For example:

The Petrol subcategory can contain several petrol transactions recorded on different dates.

### Family Member and Expense Relationship

One family member can be associated with multiple expense transactions.

This relationship helps analyze expenses according to family members.

### Vendor and Expense Relationship

One vendor can be associated with multiple household transactions.

This relationship helps identify expenditure associated with different vendors.

### Payment Method and Expense Relationship

One payment method can be associated with multiple transactions.

This relationship supports payment method analysis.

---

## 🔐 7. Data Integrity and Constraints

The project uses database constraints to maintain data consistency.

### Primary Key

Each main table contains a primary key.

A primary key uniquely identifies each record.

Examples:

- category_id
- subcategory_id
- member_id
- vendor_id
- payment_method_id
- expense_id

### Foreign Key

Foreign keys connect related tables.

For example:

The expenses table references the expense_subcategories table through subcategory_id.

This helps maintain relationships between household transactions and their associated information.

### Unique Constraint

Unique constraints prevent duplicate values in selected columns.

For example:

- Category names
- Family member names
- Vendor names
- Payment method names

### Check Constraint

The expenses table contains a check constraint requiring the expense amount to be greater than zero.

Another check constraint restricts payment status to:

- PAID
- PENDING
- PARTIAL

These constraints help maintain valid transaction information.

---

## 📊 8. Household Expense Data

The project contains household financial transactions recorded for three months.

### Analysis Period

| Month | Year |
|---|---|
| June | 2026 |
| July | 2026 |
| August | 2026 |

The dataset includes transactions related to household expenses, financial commitments, family spending, education, transportation, utilities, medical expenses, and other categories.

The SQL script includes a transaction count query that reports 62 expense records.

The project uses these records to demonstrate household financial analysis using SQL.

---

## 📈 9. SQL Analysis Performed

### 9.1 Total Expense Transaction Analysis

**Business Question:**

How many household expense transactions are recorded in the database?

**SQL Concept:**

COUNT()

**Purpose:**

To calculate the total number of financial transactions recorded in the expenses table.

This helps understand the number of transactions available for analysis.

### 9.2 Monthly Expense Analysis

**Business Question:**

How much money was spent during June, July, and August 2026?

**SQL Concepts:**

- SUM()
- COUNT()
- GROUP BY
- DATE_TRUNC()
- TO_CHAR()
- ORDER BY

**Purpose:**

To calculate total monthly expenditure and transaction counts.

This analysis helps compare household spending between different months.

### 9.3 Total Expense by Month

**Business Question:**

What is the total household expenditure for each month?

**SQL Concept:**

SUM(amount)

**Purpose:**

To calculate monthly expenditure and understand the overall household spending pattern.

### 9.4 Expense by Category

**Business Question:**

Which household expense categories have the highest expenditure?

**SQL Concepts:**

- INNER JOIN
- GROUP BY
- SUM()
- ORDER BY

**Purpose:**

To calculate total expenditure for each category.

This analysis helps identify major household spending categories.

### 9.5 Expense by Family Member

**Business Question:**

How much expenditure is associated with each family member?

**SQL Concepts:**

- INNER JOIN
- GROUP BY
- SUM()
- ORDER BY

**Purpose:**

To analyze household expenditure associated with individual family members.

This helps understand the distribution of recorded expenses across family members.

### 9.6 Recurring vs. Non-Recurring Expenses

**Business Question:**

How much expenditure is classified as recurring and non-recurring?

**SQL Concepts:**

- CASE
- GROUP BY
- SUM()

**Purpose:**

To compare recurring financial commitments with non-recurring household expenses.

Recurring expenses represent transactions classified as regular commitments.

Non-recurring expenses represent transactions classified as one-time or non-regular expenses.

### 9.7 Payment Method Analysis

**Business Question:**

Which payment methods are associated with the highest household expenditure?

**SQL Concepts:**

- INNER JOIN
- GROUP BY
- SUM()
- ORDER BY

**Purpose:**

To calculate total expenditure through different payment methods.

The project analyzes:

- UPI
- Cash
- Credit Card

This helps understand how household transactions are distributed across payment methods.

### 9.8 Highest Individual Expenses

**Business Question:**

What are the highest-value individual household expense transactions?

**SQL Concepts:**

- SELECT
- ORDER BY
- LIMIT

**Purpose:**

To identify the top 10 individual transactions according to expense amount.

This helps identify large financial transactions in the dataset.

### 9.9 Monthly Category Analysis

**Business Question:**

How does expenditure across different categories change between June, July, and August 2026?

**SQL Concepts:**

- INNER JOIN
- GROUP BY
- SUM()
- DATE_TRUNC()
- TO_CHAR()
- ORDER BY

**Purpose:**

To analyze household spending by both month and category.

This helps compare category-wise spending patterns across the three-month period.

### 9.10 Expense Classification

**Business Question:**

How can household transactions be classified according to their expense amount?

**SQL Concept:**

CASE statement

**Purpose:**

To classify individual transactions into four expense groups.

| Expense Class | Amount |
|---|---|
| Small | Less than ₹500 |
| Medium | ₹500 to less than ₹2,000 |
| High | ₹2,000 to ₹5,000 |
| Very High | More than ₹5,000 |

This classification helps organize individual transactions according to their amount.

---

## 💡 10. Key SQL Skills Demonstrated

### Database Management

- CREATE TABLE
- INSERT INTO
- Primary Key
- Foreign Key
- UNIQUE Constraint
- CHECK Constraint

### Data Retrieval

- SELECT
- ORDER BY
- LIMIT

### Data Relationships

- INNER JOIN
- Relational Database Design
- One-to-Many Relationships

### Financial Analysis

- SUM()
- COUNT()
- GROUP BY
- Monthly Expense Analysis
- Category-Wise Analysis
- Payment Method Analysis

### Conditional Analysis

- CASE Statements
- Expense Classification
- Recurring Expense Classification

### Date Analysis

- DATE_TRUNC()
- TO_CHAR()
- Monthly Grouping
- Date-Based Sorting

---

## 📌 11. Project Outcomes

This project provides practical experience in managing household financial information through PostgreSQL.

The project demonstrates how SQL can be used to:

1. Organize household transactions into relational database tables.

2. Maintain relationships between expense categories, subcategories, family members, vendors, and payment methods.

3. Record household expenses for a defined three-month period.

4. Calculate total transaction counts and monthly expenditure.

5. Analyze household expenses according to category.

6. Compare spending associated with family members.

7. Analyze recurring and non-recurring transactions.

8. Identify the payment methods used for household expenditure.

9. Identify the highest individual transactions.

10. Classify expenses according to transaction amount.

The project demonstrates the practical application of SQL for household financial data management and analysis.

---

## 🚀 12. Future Enhancements

The project can be extended with additional SQL analysis and reporting features.

Possible improvements include:

- Monthly household budget tracking.
- Budget versus actual expense analysis.
- Expense trend analysis.
- Savings analysis.
- Income and expenditure comparison.
- Pending payment analysis.
- Vendor-wise expenditure analysis.
- Additional financial reporting queries.
- Data visualization using Power BI or Tableau.
- Interactive household expense dashboard.

These enhancements can help develop the project into a more comprehensive financial analysis system.

---

## 📁 13. Project File

**File Name:** `3MonthsHouseholdExpences.sql`

The SQL file contains:

- Database table creation statements.
- Household expense category definitions.
- Expense subcategory definitions.
- Family member records.
- Payment method records.
- Vendor records.
- Household expense transaction records.
- SQL queries for household expense analysis.

---

## 🏁 Conclusion

The Household Expense Management and Analysis project demonstrates the use of PostgreSQL for relational database design, household transaction management, and SQL-based financial analysis.

By creating structured database tables and applying SQL queries, the project provides a practical understanding of household spending patterns and financial transaction analysis.

This project represents a practical SQL portfolio project and demonstrates foundational database management and data analysis skills relevant to an aspiring Data Analyst.
