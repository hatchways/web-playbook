## What is a primary key?
A 'primary key' usually refers to first column in a table in a relational database.
It's usually the `id` column. Tables use primary keys of other tables to have a
reference to them. This is called a 'foreign key'. 

Here's an example of sellers and products where the `id` is used as primary key:

`sellers` table:
| id | name  |
|----|-------|
| 1  | Sarah |
| 2  | Mike  |
| 3  | Joe   |

`products` table:
| id | title            | seller_id |
|----|------------------|-----------|
| 1  | Mike's Bread     | 2         |
| 2  | Sarah's Lemonade | 1         |
| 3  | Joe's Ice        | 3         |

To reference the seller of each product in the `products` table, 
we used the primary key of the corresponding record on the `sellers` table.

The `seller_id` would be considered a foreign key that references the `sellers`
table's primary key.

## What is the difference between soft delete and hard delete? Why would you want to do either or?
- Soft delete: 
  - Flagging row as deleted (rather than actually deleting)
  - Advantages:
    - Have record of data for future analysis
    - Don't have to worry about cascading delete on other tables
  - Disadvantages:
    - Have to take flag into account when coding, which may lead to bugs
    - Decreased performance due to memory that 'deleted' rows would be taking
    - May have high maintainability costs depending on quantity and pace of deletions on platform
- Hard delete: 
  - Permanently removing row
  - Advantages:
    - Saves space (thus increasing computation speed)
    - Can easily set cascade deletes to remove related records
      - This would be easier to code around (i.e. you'd have less conditionals)
  - Disadvantages:
    - No record of deleted data
