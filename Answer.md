**1. Explain the relationship between the "Product" and "Product_Category" entities from the above diagram.**<br>
The relationship between "Product" and "Product_Category" is a one-to-many relationship. It means that:
A single product can belong to one category. For example, a specific mountain bike can only be categorized as a "Sports Equipment" or a "Cycling" category.
A single category can contain many products. For instance, the "Sports Equipment" category might encompass various products like basketballs, tennis rackets, and yes, mountain bikes.

**2. How could you ensure that each product in the "Product" table has a valid category assigned to it?**<br>
Ways to ensure each product in the "Product" table has a valid category assigned to it are:<br>
<ol>
  <li>
    Foreign Key Constraint:
    <br>
    This is the most common and reliable method. You can define a foreign key constraint on the "CategoryID" (or similar column name) in the "Product" table. This column would reference the primary key (e.g., "CategoryID") of the "Product_Category" table.
The database management system will enforce this constraint. It will only allow inserting products with a valid category ID that already exists in the "Product_Category" table. Any attempt to insert a product with an invalid category ID will be rejected.
    
  </li>
  <li>
    Data Validation in Application Logic:<br>
During application development, you can implement data validation rules before inserting a new product.
You can check if the provided category ID exists in the "Product_Category" table before adding the product to the "Product" table.
This approach offers flexibility, but it relies on proper implementation within the application and might require additional coding effort.
  </li>
  <li>
    Default Category:<br>
You can define a default category (e.g., "Uncategorized") in the "Product_Category" table.
If a product is added without specifying a category, the system can automatically assign it the default category.
This is a fallback option, but it's important to have a process for reviewing and assigning proper categories to uncategorized products later.
  </li>
</ol>

