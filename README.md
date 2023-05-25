# Web-dev learning checkpoints and notes
## FastAPI
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
  

## HTML/CSS/JavaScript
- The main components of HTML are tags and attributes. <tag attribute="value"> display content </tag> (This whole thing is called an **element**)
  - Multiple attributes are separate by just a space.
- HTML is a markup language to create the structure of a webpage.
- CSS is a markup language used to style a webpage. HTML reads in CSS to style the page. 
- The two is used in conjunction, but the convention is to decouple them as much as possible. 
  - We can use the *style attribute* in HTML tags  
  - We can use the *style tag* in the head tag to change other HTML tags
  - We can create **classes** that are a predefined set of stylings that can be applied to tags. These classes can then be put into a styles.css *stylesheet*.
    - The CSS **class selector** matches elements based on their class attribute.
- npm is a package manager for JS.
 

## React
- [x] Read through React Quickstart
  - React is a JavaScript library for building user interfaces and web apps.
  - React apps are made out of **components**. A component is a piece of the UI (user interface) that has its own logic and appearance. These components are **JavaScript functions** that return **markup**.
    - React components must start with a capital letter. HTML tags always start with a lower case.
  - The markup language that React uses is **JSX**, a syntax extension for JavaScript.
  - A **JSX element** is a combination of JavaScript code and HTML tags that describes what you’d like to display.
    - React components must only return *one* JSX element. To do this, we use Fragment  
  - JSX elements have **properties**, or **props**, that are like HTML tag **attributes**. These are just key value pairs.
  - **className** is the React equivalent to *class* in JS (because class is a keyword in JS)
  - For nested components, there is more terse syntax <Component /> instead of <Component> </Component>.
    - Nested components function like tags, where the attributes are the function inputs. 
  - Curly braces are used to "exit out of JSX and enter into JS". Mainly used for refering to variables.
  - User interactions is handled with **events**. Within the JSX element, we can define user interactions which it will listen for.
    - A button JSX element has things like onClick. 
    - **Events** are written in camel case in React. (HTML is all lower case)
  - React lets you define **event handlers** within components, which are just user defined JS functions detailing what happens when an event occurs.
    - The convention is to prefix the function within the component with "handle".
    - Event handlers are passed as *props* to the *JSX element* based on the *event*. It can also just be defined inline with an **arrow function**
      - Do not call the function, they must only be **passed** as a prop. 
  - To remember things, components use **state**.
    - React provides a special function called **useState** that declares a state variable for that component. *The scope of the state variable is private to the component that defined it.*
    - const is used here in JS to block scope and change the value of a variable only with the specified function.
    - Lifting state into a parent component from its children is good practice.
      - We can then pass values as a *prop* to the children. What is often needed as well is passing an **event handler** as a **prop** to the child component, such that it gets triggered based on an event (The event is not pertaining to the parent so to speak, but the scope of the state is in the parent. Therefore the event handler needs to be passed down to the child because that is where the event is triggered)
  - Functions starting with *use* are called **Hooks**. They are special in that they can only be called at the top of your components/other Hooks.
    - useState is an inbuilt Hook provided by React.
    -   
