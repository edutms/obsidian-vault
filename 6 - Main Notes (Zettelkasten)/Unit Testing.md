2025-08-18 16:43

### Status: #baby

### Tags: [[data-engineering]]

# What is  Unit Testing?

### What Unit Testing means in data

A **unit** will be a transformation, function or SQL query that outputs a predictable result given we have known inputs.

Implementing unit testing will allow us to make sure that:
- Each transformation behaves accordingly
- Data integrity is preserved
- Edge cases and bad data does not break the workflow


## Examples

#### Transformation functions
- for example, a function that normalizes company names should always yield the same output
	- "Gooogle Inc --> Google"

#### SQL Queries
- A join should not multiply rows in the table
	- if it does, maybe there was an upstream failure
- A filter should exclude *null* values as intended

#### Data Quality rules
- Columns expected to be unique values having no duplicates
- Dates are contained in a given date range
- Categorical fields only contains expected values


### Know frameworks
- [Great Expectations]
- **dbt tests** (e.g., `unique`, `not_null`, `accepted_values`)






# References









