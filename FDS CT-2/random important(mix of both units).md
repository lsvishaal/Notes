# 1. difference between match and search operation in RE



**Match Operation:**

1. **Start Anchored:** `match` checks if the pattern matches the entire string from the beginning, anchoring the match to the start of the string.
    
2. **Return Value:** It returns a match object if the pattern matches the beginning of the string, or `None` if no match is found.
    

**Search Operation:**

1. **Anywhere in String:** `search` searches for the pattern anywhere within the string, not necessarily at the beginning.
    
2. **First Occurrence:** It returns a match object for the first occurrence of the pattern within the string, or `None` if there's no match..

# 2. convert python dict to json string and vice versa

**Python Dictionary to JSON String:**

1. **Import JSON Module:** Import the `json` module in Python.
2. **Use `json.dumps()`:** Use `json.dumps()` to convert a Python dictionary into a JSON-formatted string.

**JSON String to Python Dictionary:**

1. **Import JSON Module:** Import the `json` module in Python.
2. **Use `json.loads()`:** Use `json.loads()` to parse a JSON string into a Python dictionary.

# 3. how can you send data as a part of get request in python request library?

**1. Import the `requests` Library:**

- Start by importing the `requests` library at the beginning of your Python script.

**2. Create a Parameters Dictionary:**

- Create a Python dictionary where each key represents a parameter name, and its corresponding value is the data you want to send.

**3. Use `params` Parameter:**

- When making a GET request using `requests.get()`, pass the parameters dictionary as the `params` parameter. This attaches the parameters to the URL.

**4. Automatic URL Encoding:**

- The `requests` library automatically URL-encodes the parameters, ensuring proper formatting for the GET request URL.

# 4. what is django and why is it used in web development?

1. **Python Web Framework:**
   - Django is a Python-based web framework designed for building web applications efficiently.

2. **Rapid Development:**
   - It facilitates rapid development by offering pre-built components like an ORM, forms, and authentication.

3. **Structured Codebase:**
   - Django enforces a structured codebase, promoting maintainability and scalability.

4. **Security Focus:**
   - Django incorporates security measures to protect against common web vulnerabilities, enhancing the safety of web applications.

# 5. explain query-set in django, How does it differ from list and dictionary?


1. **Database Query Representation:**
- A Django QuerySet is a dynamic representation of a database query in Django, allowing you to interact with the database using Python code.

2. **Database Integration:**
- QuerySets directly interact with the database, making them efficient for data retrieval, filtering, and manipulation at the database level.

3. They are different from lists because they do not interact with databases and require loading data from the database into memory.
4. They are different from dictionary because they do not have inherent database integration and are limited in their querying capabilities compared to QuerySets.

# 6. Evaluate key concept of django including settings.py, urls.py, views.py , models.py


1. **Django Project Structure:**
   - Organized directory layout for apps, settings, and templates.

2. **manage.py:**
   - CLI tool for project management tasks, like starting the server.

3. **settings.py:**
   - Central configuration file for project settings and customization.

4. **urls.py:**
   - URL pattern definitions for routing HTTP requests.

5. **views.py:**
   - Functions that handle HTTP requests and generate responses.

6. **models.py:**
   - Python classes defining database structure, fields, and relationships.

7. **URL Routing:**
   - Maps URLs to view functions, separating routing logic.

8. **View Functions:**
   - Process specific HTTP requests, encapsulating application behavior.

9. **Template Rendering:**
   - Generates dynamic HTML by combining templates and Python data.

10. **Database Models:**
    - Python representations of database tables, with fields and relationships.

//11. **ORM (Object-Relational Mapping):**
    - Abstraction layer for database interactions using Python code.

12. **Configuration and Settings:**
    - Centralized hub (settings.py) for project customization and adaptability.