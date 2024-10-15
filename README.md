**README: SQL PROJECT Solution**
Overview
This document provides details on the SQL queries written to solve the given assignment based on a commercial database schema. The schema contains the following tables:

CATEGORIES: (CATEGORY_CODE, CATEGORY_NAME, DESCRIPTION)
CUSTOMERS: (CUSTOMER_CODE, COMPANY, ADDRESS, CITY, POSTAL_CODE, COUNTRY, PHONE, FAX)
ORDERS: (ORDER_NUMBER, CUSTOMER_CODE, EMPLOYEE_NUMBER, ORDER_DATE, SHIP_DATE, SHIPPING_COST)
ORDER_DETAILS: (ORDER_NUMBER, PRODUCT_REF, UNIT_PRICE, QUANTITY, DISCOUNT)
EMPLOYEES: (EMPLOYEE_NUMBER, REPORTS_TO, LAST_NAME, FIRST_NAME, POSITION, TITLE, BIRTH_DATE, HIRE_DATE, SALARY, COMMISSION)
SUPPLIERS: (SUPPLIER_NUMBER, COMPANY, ADDRESS, CITY, POSTAL_CODE, COUNTRY, PHONE, FAX)
PRODUCTS: (PRODUCT_REF, PRODUCT_NAME, SUPPLIER_NUMBER, CATEGORY_CODE, QUANTITY, UNIT_PRICE, UNITS_IN_STOCK, UNITS_ON_ORDER, UNAVAILABLE)
This assignment involves a series of SQL queries designed to extract specific insights from the database by performing operations such as filtering, aggregation, and formatting.

**Instructions**
To execute the provided queries, you should first ensure the database schema is loaded using the commercial.sql script.

Once the database is set up, you can run the individual queries as outlined below:

**Queries**
Display Senior Male Employees with High Net Salary

Query filters male employees with a net salary (salary + commission) greater than or equal to 8000.
Columns: Employee Number, First Name, Last Name (formatted with LPAD/RPAD), Age, and Seniority.
Display Products Meeting Specific Criteria

**Conditions:**
Quantity packaged in bottles.
The third character in the product name is 't' or 'T'.
Supplied by suppliers 1, 2, or 3.
Unit price between 70 and 200.
Units ordered is specified (not null).
Columns: product number, product name, supplier number, units ordered, and unit price.
Display Customers in Same Region as Supplier 1

The query finds customers who share the same country, city, and the last three digits of the postal code as supplier 1, utilizing a single subquery.
Columns: All customer table columns.
New Discount Rate for Specific Order Numbers

For each order number between 10998 and 11003:
Display the new discount rate based on the total order amount before discount.
Display a note for the discount rate application.
Columns: order number, new discount rate, and discount rate application note.
Display Beverage Suppliers

The query retrieves suppliers who supply beverages.
Columns: supplier number, company, address, and phone number.
Display Berlin Customers Who Ordered at Most One Dessert Product

The query filters customers from Berlin who have ordered 0 or 1 dessert product.
Column: customer code.
Display French Customers and Their Orders on Mondays in April 1998

The query finds customers residing in France and the total order amount they placed every Monday in April 1998, including those who haven’t placed any orders.
Columns: customer number, company name, phone number, total amount, and country.
Display Customers Who Have Ordered All Products

The query lists customers who have ordered all available products.
Columns: customer code, company name, and telephone number.
Display the Number of Orders per French Customer

The query retrieves the number of orders placed by each French customer.
Columns: customer code and number of orders.
Display Number of Orders in 1996, 1997, and Their Difference

The query displays the number of orders placed in 1996, the number of orders placed in 1997, and the difference between these two values.
Columns: orders in 1996, orders in 1997, and the difference.
Database Schema Details
CATEGORIES:

Holds the details of product categories.
Fields: CATEGORY_CODE, CATEGORY_NAME, and DESCRIPTION.
CUSTOMERS:

Contains customer details.
Fields: CUSTOMER_CODE, COMPANY, ADDRESS, CITY, POSTAL_CODE, COUNTRY, PHONE, FAX.
ORDERS:

Stores order details such as order date, shipping date, and shipping cost.
Fields: ORDER_NUMBER, CUSTOMER_CODE, EMPLOYEE_NUMBER, ORDER_DATE, SHIP_DATE, SHIPPING_COST.
ORDER_DETAILS:

Holds details about products ordered, including quantity, unit price, and discount applied.
Fields: ORDER_NUMBER, PRODUCT_REF, UNIT_PRICE, QUANTITY, DISCOUNT.
EMPLOYEES:

Contains employee details, including supervisor relationships and salaries.
Fields: EMPLOYEE_NUMBER, REPORTS_TO, LAST_NAME, FIRST_NAME, POSITION, TITLE, BIRTH_DATE, HIRE_DATE, SALARY, COMMISSION.
SUPPLIERS:

Stores details about suppliers, including contact information.
Fields: SUPPLIER_NUMBER, COMPANY, ADDRESS, CITY, POSTAL_CODE, COUNTRY, PHONE, FAX.
PRODUCTS:

Contains product information, including quantity in stock, unit price, and supplier details.
Fields: PRODUCT_REF, PRODUCT_NAME, SUPPLIER_NUMBER, CATEGORY_CODE, QUANTITY, UNIT_PRICE, UNITS_IN_STOCK, UNITS_ON_ORDER, UNAVAILABLE.
How to Run
Ensure the SqlProject.sql script is executed to create the database schema.
Copy the provided SQL queries into your SQL client or script file.
Execute the queries one by one to retrieve the required results.
**Conclusion**
This assignment demonstrates a range of SQL capabilities, including filtering, aggregation, conditional logic, and subqueries to solve practical database queries. The database schema provided a structured way to interact with commercial data and gain insights using SQL.
