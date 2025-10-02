2025-01-20 09:06

### Status: #child

### Tags: [[data-engineering]]

# Data Normalization

#### What is Data Denormalization?
Is a data engineering technique used to alter database structures. It is the process of organizing data in the database aiming to reduce redundancy and improve data integrity. It also involves decomposing tables into smaller, better-structured tables and defining relationships between them.

### Normal Forms

testing git on obsidian

-

#### 1NF
- Each column contains atomic and indivisible values
- Each column contains values of a single type
- Each column has a unique name
- The order of rows and columns does not matter

```
--bad example

CREATE TABLE customers_bad (
	customer_id INT,
	name VARCHAR(100),
	phone_numbers VARCHAR(255)
);

-- good example

CREATE TABLE customers (
	customer_id INT PRIMARY KEY,
	name VARCHAR (100)
	);

CREATE TABLE customer_phones (
	customer_id INT,
	phone_number varchar(15),
	phone_type VARCHAR(20),
	FOREIGN KEY (customer_id) references customers(customer_id)
);
```

#### 2NF
- must be 1NF
- All non-key attributes must be fully functionally dependent on the primary keys
- Eliminates partial dependencies


```

-- BAD: Partial dependency exists
CREATE TABLE order_items_bad (
    order_id INT,
    product_id INT,
    product_name VARCHAR(100),    -- Depends only on product_id
    product_category VARCHAR(50), -- Depends only on product_id
    quantity INT,                 -- Depends on both order_id and product_id
    unit_price DECIMAL(10,2),     -- Depends only on product_id
    PRIMARY KEY (order_id, product_id)
);

------------

-- GOOD: Separate tables eliminate partial dependencies
CREATE TABLE orders (
    order_id INT PRIMARY KEY,
    customer_id INT,
    order_date DATE
);

CREATE TABLE products (
    product_id INT PRIMARY KEY,
    product_name VARCHAR(100),
    product_category VARCHAR(50),
    unit_price DECIMAL(10,2)
);

CREATE TABLE order_items (
    order_id INT,
    product_id INT,
    quantity INT,
    PRIMARY KEY (order_id, product_id),
    FOREIGN KEY (order_id) REFERENCES orders(order_id),
    FOREIGN KEY (product_id) REFERENCES products(product_id)
);

```

#### 3NF
- Must be 2NF
- No transitive dependencies (non-key attributes must not depend on non-key attributes)

```
-- BAD: Transitive dependency exists
CREATE TABLE employees_bad (
    employee_id INT PRIMARY KEY,
    name VARCHAR(100),
    department_id INT,
    department_name VARCHAR(100),  -- Depends on department_id, not employee_id
    department_budget DECIMAL(12,2) -- Depends on department_id, not employee_id
);

--- department_name and department_budget depend on department_id, not on employee_id
--- creates redundancy and potential inconsistencies

--------

-- GOOD: Eliminate transitive dependencies
CREATE TABLE departments (
    department_id INT PRIMARY KEY,
    department_name VARCHAR(100),
    department_budget DECIMAL(12,2)
);

CREATE TABLE employees (
    employee_id INT PRIMARY KEY,
    name VARCHAR(100),
    department_id INT,
    FOREIGN KEY (department_id) REFERENCES departments(department_id)
);

```