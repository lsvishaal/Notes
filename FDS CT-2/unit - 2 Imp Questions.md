# 4 marks:
## 1. Debugging in Python using pdb

1. **Set Breakpoints**: Pause your code at specific points with `import pdb; pdb.set_trace()`, allowing you to examine what's happening.

2. **Step Through Code**: While paused, move through your code step by step to understand its flow.

3. **Inspect Variables**: Use the `p` command to check variable values during debugging.

4. **Continue Execution**: Resume program execution after inspection using the `continue` command.

## 2. JSON - Read, Write, Parse

1. **JSON Format**: JSON (JavaScript Object Notation) is a widely used format for structured data, ideal for data exchange between applications.

2. **Reading JSON**: In Python, use `json.load()` to read JSON from a file, converting it into a dictionary.

3. **Writing JSON**: Use `json.dump()` to write data to a JSON file, taking a dictionary and saving it in JSON format.

4. **Parsing JSON Strings**: Employ `json.loads()` to parse JSON strings into a dictionary.

5. **Converting to JSON Strings**: Utilize `json.dumps()` to convert a Python dictionary into a JSON-formatted string.

## 3. Limitations of JSON

1. **No Native Comments**: JSON lacks built-in support for comments within data, making documentation challenging.

2. **No Data Types for Objects**: JSON objects only support string keys, limiting key data types to strings.

3. **No Support for Metadata**: JSON lacks a standardized way to include metadata or data validation rules.

4. **No Inherent Schema**: JSON doesn't enforce a specific structure or data type constraints, making it challenging to standardize data.

## 4. Floating Point and Arithmetic in JSON

1. **Precision Limitation**: JSON can't represent extremely precise numbers due to its limited decimal places.

2. **Possible Rounding**: Arithmetic with JSON floating-point numbers can introduce small rounding errors.

3. **Scientific Notation**: JSON allows numbers to be written in scientific notation (e.g., 1.23e-4 for 0.000123).

4. **Use Tolerance**: It's advisable to compare JSON floating-point numbers with a tolerance threshold to account for small differences.

## 5. Regular Expressions - Find All, Search, Split Operations

1. **Pattern Matching**: Regular expressions define patterns for text matching, allowing you to find specific sequences in text.

2. **Find All**: This operation locates all instances of a pattern in text and returns them as a list.

3. **Search**: The "Search" operation finds the first occurrence of a pattern and provides its position in the text.

4. **Split**: "Split" uses regex patterns to divide text into parts wherever the pattern is matched, useful for tokenization.


# 12 marks:
## UNIT II

## 1. explain CRUD operations in python using mysql.



**Create (C)**:

1. **Connect to Database**: Establish a connection to your MySQL database using a library like `mysql-connector-python` or `pymysql`.

2. **Create SQL Query**: Define an SQL query to insert new data into a table. For example, `INSERT INTO tablename (column1, column2) VALUES (value1, value2)`.

3. **Execute Query**: Use the database connection to execute the SQL query. This inserts the new data into the specified table.

4. **Commit Changes**: After executing the query, commit the changes to the database using `commit()` to make the data permanent.

**Read (R)**:

5. **Create SQL Query**: Construct an SQL query to retrieve data from a table. For instance, `SELECT * FROM tablename WHERE condition`.

6. **Execute Query**: Use the database connection to execute the SQL query, which fetches the desired data.

7. **Fetch Data**: Retrieve the data from the query result, often as a list of dictionaries or tuples, and process it in Python.

**Update (U)**:

8. **Create SQL Query**: Formulate an SQL query to update existing data in a table. For example, `UPDATE tablename SET column1 = new_value WHERE condition`.

9. **Execute Query**: Execute the SQL update query to modify the data in the table.

10. **Commit Changes**: After updating, commit the changes to save them permanently to the database.

**Delete (D)**:

11. **Create SQL Query**: Design an SQL query to delete specific data from a table. For instance, `DELETE FROM tablename WHERE condition`.

12. **Execute Query**: Execute the SQL delete query to remove the specified data from the table.


## 2. refer notes or skip



## UNIT III
## 1. explain about MVC in django.

Certainly! Here are the 12 points about MVC in Django, each in one line:

**Model (M):**

1. Manages data, serves as a data access layer, and represents database interactions.
2. Responsible for maintaining logical data structure and data validation.
3. Interacts with databases using Object-Relational Mapping (ORM).

**View (V):**

4. Corresponds to the user interface, controlling what users see in the browser.
5. Composed of HTML, CSS, and JavaScript, defining UI presentation.
6. Includes placeholders for dynamic data insertion from the Model.

**Template (T):**

7. Represents the presentation layer, handling UI aspects.
8. Contains both static and dynamic parts in HTML output.

**Controller (Request Handling):**

9. Django acts as the controller, handling request processing.
10. Utilizes URL mapping to determine which View (Template-handling function) to call.

**Request-Response Flow:**

11. Users make requests to Django, which acts as the controller.
12. If URL maps to a View, it interacts with the Model, renders a Template, and sends it as a response.

Django's MVT closely aligns with MVC, with Models handling data, Templates handling UI, and Django managing request processing and routing.

# Using django , populate database and use model fields

skip xd