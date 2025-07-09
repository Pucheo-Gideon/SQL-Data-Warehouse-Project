# Data Warehouse and Analytics Projects 

### Objective: 
Build a consolidated, modern Data Warehouse with SQL including Data wrangling techniques for reporting and business decision making

## General Principles 
-  Naming conventions: Use snake-case with lowercase letters and underscore(_) to separate words.
-  Language: Use English for all names.
-  Avoid reserves words: Do not use SQL reserves for naming objects. 

# Table Naming Conventions
## Bronze Rules 
-  All name must start with the source system name and table names must march their original names without renaming
-  #### <sourcesystem>_<entity> 
      -  `<sourcesystem>_<entity>`: Name of thesource system (e.g., `crm`, `erp`).
      -  `<entity>` : Exact table name from the source system.
      -  Example `crm_customer_info` → Customer information from the CRM system.
   
## Gold Rules 
-  All names must use meaningful, business-aligned names for tables, starting with the category prefix
-  `<category>_<entity>`
      - `<category>`: Describes the role of the table, such as `dim` (dimension) or `fact` (fact table)
      - `<entity>`: Descriptive name of the table, aligned with the business domain (e.g customers, products, sales)
      -  Examples: 
            -  `dim_customers` → Dimension table for customer data. 
            -  `fact_sales` → Fact Table containing sales transactions.

  #### Glossary of Category Patterns

  | Pattern | Meaning | Examples | 
  | --------  | ------- | -------- |
  | `dim_` | Dimension table | `dim_customer`, `dim_product` |
  | `fact_` | Fact table | `fact_sales` |
  | 'agg_` | Aggregated_table | `agg_customers`, `agg_sales_monthly` |
            
  
