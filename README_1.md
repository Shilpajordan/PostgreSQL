## Why Use Postgres?
- Postgres is an object relational database that is just as fast as MySQL that adheres more closely to SQL standards and excels at concurrency.
- Postgres is also superior at avoiding data corruption.
- Postgres also provides more advanced data types and allows for the creation of custom types, operators and index types. 
- Postgres is normally the best option when extensibility, scalability and data integrity are most important to you. 
## What is a Database
- A database is data that is structured into rows and columns like a spreadsheet. To receive or change data in a database you send it commands called queries. 
- The database in turn returns a result based on that request.
- Databases contain many tables of data organized into rows and columns. Each column represents one type of data the database stores. 
- Each row contains multiple pieces of data specific to each entity you are describing.
-  For example we store information on students here. Each individual value stored is called a cell. 
- Primary keys are used to define unique entities in your tables. Here id provides a unique value associated with each student.
## How to design a DB
- 1 Table represents 1 real world Object
- Columns store 1 piece of information
- How do tables relate
- Reduce redundant data
## CHARACTER TYPES
- char(5) : Stores up to a maximum number of 5 characters.
- Varchar: stores any length of characters
- Varchar(20): Stores up to 20 characters
- Text: Store any length of characters
## NUMERIC TYPES
- Serial: Whole number that also auto increment. Always used for column ids
    - Small serial: 1 to 32,767
    - Serial: 1 to 2147483647
    - Bigserial: 1 to 9223372036854775807
- Integer: whole numbers only. always used when you don't need a decimal
    - Smallint : -32,768 to 32, 767
    - Integer : -2,147,583,648 to 2,174,483,647
    - Bigint : -9223372036854775808 to 9223372036854775807
- Floats: numbers with decimals
    - Decimal : 131072 whole digits and 16383 after decimal
    - Numeric : 131072 whole digits and 16383 after decimal
    - Real : 1E-37 to 1E37 (6 places of precision)
    - Double Precision : 1E-307 to 1E308 (15 places of precision) Used when decimal doesn’t have to be very precise
    - Float : Same as double
- Boolean: True, False or null
    - True, 1, t, y, yes, on
    - False, 0, f, n, no, off
    - null
- Date / Time 
- DATE: Format YYYY-MM-DD
    - No matter what format you enter you get this : 1974-12-21
- TIME
- TIME WITHOUT TIME ZONE (Default)
    - ‘1:30:30 PM’:: TIME WITHOUT TIME ZONE -> 13:30:30
    - 01:30 AM EST -> 01:30-5:00 (UTC Format)
    - 01:30 PM PST -> 01:30-8:00
    - 01:30 PM UTC -> 01:30+00:00
    - ’01:30:30 PM EST’::TIME WITH TIME ZONE -> 13:30:30-5:00
- TIMESTAMP
    - ‘DEC-21-1974 1:30 PM EST’::TIMESTAMP WITH TIME ZONE -> 1974-12-21 13:30-5:00
- INTERVAL
    - Represents a duration of time
    - ‘1 day’::INTERVAL -> 01:00
    - ‘1 D 1 H 1 M 1 S’::INTERVAL -> 01:01:01:01
    - You can add and subtract intervals
    - You can add or subtract intervals from dates
    - (‘DEC-21-1974 1:30 PM EST’::TIMESTAMP WITH TIME ZONE) – (‘1 D’::INTERVAL)
- Also other data types include : Currency, Binary, JSON, Range, Geometric, Arrays, XML, UUID
## WHERE
- WHERE is used to define which rows are included in the results based on a condition
## Conditional Operators
- = : Equal
- < : Less than
- '>' : Greater than
- <= : Less than or Equal
- '>=' : Greater than or Equal
- <> : Not Equal
- != : Not Equal
## DESC 
- The following gives results from high to low
## ASC
- The following gives results from low to high
## LIMIT
- LIMIT limits the number of rows in the result
## CONCAT
- We can use CONCAT to merge to columns. We can then use AS to define a new column name.
## IN 
- The IN phrase can be used to test if a value is in a list. 
## Getting Data from Multiple Tables