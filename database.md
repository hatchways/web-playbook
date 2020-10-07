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

## What is normalization?
Normalization is a database design technique that aims to eliminate redundancy in data.
This allows you to avoid anomalies when doing INSERT, UPDATE, and DELETE operation where
you may change data in one part and forget to change it in another.

Normalization advances in terms of 'normal forms'; the higher up the form, the more normalized
a database is. Read more about normal form hierarchy and database normalization [here](https://en.wikipedia.org/wiki/Database_normalization#Normal_forms).

