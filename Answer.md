 Answer 1 - 
      Relationship Between “Product” and “Product_Category” Entities:-
 
    - In the given database schema diagram, the “Product” and “Product_Category” entities are 
      related through a foreign key relationship.Specifically, the “Product” entity has an 
      attribute called “category_id,” which serves as a foreign key referencing the primary key 
      of the “Product_Category” table.
    - This relationship indicates that each product in the “Product” table is associated with a 
      specific category defined in the “Product_Category” table.In other words, the “category_id” 
      in the “Product” table points to the corresponding category in the “Product_Category” table.

    
 Answer 2 - 
   To ensure that each product in the “Product” table has a valid category assigned, consider 
   the following steps:

 1. Data Integrity Constraints: Implement data integrity constraints in the database schema.Specifically:-
    - Set the “category_id” column in the “Product” table as a foreign key referencing the 
      primary key (“category_id”) in the “Product_Category” table.
    - Use the NOT NULL constraint to ensure that every product must have a valid category 
      assigned (i.e., the “category_id” cannot be null).
 2. Validation Logic in Application Code:
    - When inserting or updating product records, validate that the provided “category_id” 
      corresponds to an existing category in the “Product_Category” table.
    - If the category is not valid, reject the operation or prompt the user to select a valid 
      category.
 3. Regular Data Audits:
    - And at last periodically audit the data to identify any inconsistencies (e.g., products 
      with invalid or non-existent category IDs etc).
    - And correct any discrepancies found during the audit process.
