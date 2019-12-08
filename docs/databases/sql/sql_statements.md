## SQL statements syntax

List of sql commands: https://www.codecademy.com/articles/sql-commands

### 1. CREATE

A statement is text that the database recognizes as a valid command. Statements always end in a semicolon `;`.

    CREATE TABLE table_name (
    column_1 data_type, 
    column_2 data_type, 
    column_3 data_type
    );


Let’s break down the components of a statement:

1. `CREATE TABLE` is a clause. Clauses perform specific tasks in SQL. By convention, clauses are written in capital letters. Clauses can also be referred to as commands.

2. table_name refers to the name of the table that the command is applied to.

3. (`column_1 data_type`, `column_2 data_type`, `column_3 data_type`) is a parameter. A parameter is a list of columns, data types, or values that are passed to a clause as an argument. Here, the parameter is a list of column names and the associated data type.

The structure of SQL statements vary. The number of lines used does not matter. A statement can be written all on one line, or split up across multiple lines if it makes it easier to read.

example:

    CREATE TABLE students (
        id INTEGER,
        name TEXT,
        age INTEGER
    );

### 2. INSERT

The `INSERT` statement inserts a new row into a table. You can use the `INSERT` statement when you want to add new records.

    example:

    1. Insert single row in the created table

        INSERT INTO students (id, name, age) 
        VALUES (1, 'Jon Doe', 22);

    2. Insert multiple vaules in the created table

        INSERT INTO table (id, name, age)
        VALUES
        (2, 'Micheal Scott', 50),
        (3, 'Dwight Schrute', 40),
        (4, 'Sheldon Cooper', 35);


### 3. SELECT

`SELECT` statements are used to fetch specific or all data from a database. 


    examples:

    1. SELECT returns all data in the name column of the students table.

       SELECT name FROM students;

    2. SELECT returns all data from all the columns of the students table. 

       SELECT * FROM students;   

       
       * is a special wildcard character allows you to select every column in a table without having to name each one individually.

### 4. ALTER

The `ALTER TABLE` statement adds a new column to a table. You can use this command when you want to add columns to a table. 

    examples:

    1. The statement below adds a new column student_major to the students table.

        ALTER TABLE students
        ADD COLUMN student_major TEXT;


`NULL` is a special value in SQL that represents missing or unknown data. Here, the rows that existed before the column was added have `NULL` values for `student_major`.


!!! warning

    you cannot specify what position to add a column to a table.
    
    By default, a new column will always be added at the end of the table.
    
    If column order is very important, then an alternative is to create a new table and add the columns in the specific order they should appear.


### 5. UPDATE

The `UPDATE` statement edits a row in a table. 
You can use the `UPDATE` statement when you want to change existing records.

`WHERE` is a clause that indicates which row(s) to update with the new column value.


    examples:

        UPDATE students 
        SET student_major = 'Physics' 
        WHERE id = 4;


!!! faq

    **Question:** How is ALTER different from UPDATE?

    **Answer:**

    Although similar in the sense that both statements will modify a table, these statements are quite different.

    The **ALTER** statement is used to modify columns. With **ALTER**, you can add columns, remove them, or even modify them.

    The **UPDATE** statement is used to modify rows. However, **UPDATE** can only update a row, and cannot remove or add rows


### 6. DELETE

The `DELETE` FROM statement deletes one or more rows from a table. 
You can use the statement when you want to delete existing records.


    examples:

    1. delete all records in the students table with no student_major :

        DELETE FROM students 
        WHERE student_major IS NULL;

        WHERE is a clause that lets you select which rows you want to delete. 
        Here we want to delete all of the rows where the student_major column IS NULL .
        
        IS NULL is a condition in SQL that returns true when the value is NULL and false otherwise.



    2. delete a specific number of rows, Deleting rows 1 and 3 with student_major is null.

        DELETE FROM celebs
        WHERE id in (1,3) and student_major IS NULL;



### 7. CONSTRAINTS

`CONSTRAINTS` that add information about how a column can be used are invoked after specifying the data type for a column. 
They can be used to tell the database to reject inserted data that does not adhere to a certain restriction. The statement below sets constraints on the celebs table.


    example:

        CREATE TABLE awards (
        id INTEGER PRIMARY KEY,
        recipient TEXT NOT NULL,
        award_name TEXT DEFAULT 'Grammy'
        );




!!! faq

    **Question:** What are some reasons to apply constraints to a table?

    **Answer:**

    Applying constraints to a table can be useful, and provide some important benefits such as reliability and consistency of your data. The following are a few reasons you might consider for applying constraints to a table.

    One reason for adding constraints is to prevent invalid data in the table. This is very important, because invalid data can cause issues and unexpected results from calculations. We do not have to worry about new data being added that might otherwise violate our constraints and cause bigger issues.

    Similar to the previous point, constraints can let us prevent missing data, which is usually filled as NULL within the table. Instead of having missing values set to NULL, we can set constraints so that the missing values are given some default value instead, like 0. This can make some calculations easier to do.

    Another important reason to add a constraint is for uniqueness, usually in the form of values like the id, or identifier column. By using a constraint like the PRIMARY KEY, we can ensure that every row has their own unique id value.