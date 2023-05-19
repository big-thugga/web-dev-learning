# Web-dev learning checkpoints
## Backend using FastAPI
- [x] Read up on FastAPI
  - Better than Django and Flask.
- [x] Go through the demo on homepage and run my first ever web server!
- [x] Go through the Python Types Intro page: https://fastapi.tiangolo.com/python-types/ 
  - Python type hinting is very powerful in the FastAPI framework. Use the standard typing module for type hinting
  - Simple types, generic types and type parameters.
  - Optional and Union
  - pydantic is a library for data validation. FastAPI is all based on pydantic. Uses object oriented programming
      - Has inbuilt data type validation and conversion/parsing with pydantic (Type hints are automatically enforced)
      - Provides automatic type hints, auto completions, searching and errors (Especially for bodies)
- [ ] Go through the Tutorial - User Guide page
  - app instance of the FastAPI class
  - Path operation decorator and path operation function  
    - Path operation decorator specifies the path and the operation (HTTP request method) 
    - Path operation function defines what happens when the path and operation specified by the decorator occurs
  - Path parameters 
    - Specified by the path operation decorator
  - Query parameters
    - Parameters in the path operation function that is not in the path
    - Goes after the ? in the URL and is separated by & characters
    - Query parameters are required unless there is a default value. If you just want to make it optional without a specific value, use None
  - Request body 
    - Since request bodies is sending data, should use POST, PUT, DELETE or PATCH
    - Request bodies in FastAPI is built using Pydantic, and inherits from the BaseModel class. This Pydantic approach provides a whole suite of added functionality
    - Declared in the path operation function, just like a path or query parameter
  - Path operation functions can take multiple path and query parameters, on top of a body. If the parameter is declared in the path, it is used as a path parameter. If it is a singular type, it is used as a query parameter. If it is of type Pyndatic model, it is interpreted as a body request.
  
  


- [ ] Create the front page of the game (Or the root)
