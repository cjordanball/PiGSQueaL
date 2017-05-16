# Postgres Database
[toc]
## Installation
1. The easiest way to get set up on a MacOs with Postgres is to go to **postgresapp.com** and download the Postgres.app.

2. Click on the download, then drag into the Applications folder in the little box. That's it!

3. In addition, it makes things easier to work with to get an application called Postico, which provides a GUI environment for working with Postgres.

4. Finally, be sure to set up the correct PATH information in your terminal profile into order to be able to use the command line tools.

## Creating and Removing Database
1. From the command line, one can create a new database with the following command, if everything is installed correctly:
    ```
    ~ createdb [database name]
    ```
2. To delete (or "Drop") a database from the command line, type:
    ```
    ~ dropdb [database name]
    ```

## Accessing the Database
1. From the command line, once a database is created, it can be accessed by:
    ```
    psql [database name]
    ```
2. To change the database from the command line, use:
    ```
    \connect [database name]
    ```

## Creating  or Removing a Table
1. Use the following SQL command to create a table:
    ```sql
    CREATE TABLE tableName();
    ```
    The parens after the table name can be empty, or can contain columns to include in the table (name and data type);
    
2. Removing a table from a database is easy, just drop it:
    ```sql
    DROP TABLE tablename;
    ```
    
## Adding Data to Table
1. To add a row of data to a table, use the **INSERT INTO** statement, with the keyword **VALUES** to signal the data:
    ```sql
    INSERT INTO my_contacts (last_name, first_name, age, city, state)
        VALUES('Ball', 'Jordan', 55, 'Richmond', 'VA');
    ```
    Note that values have to be in the same order as the columns listed. However, the columns listed don't have to be in the order they appear in the database. Also, columns can be omitted.
    
