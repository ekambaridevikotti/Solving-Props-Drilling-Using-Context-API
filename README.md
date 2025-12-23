# 🚀 Solving Props Drilling Using React Context API

## 📌 Project Overview

This project demonstrates how React Context API can be used to eliminate props drilling in a deeply nested component structure.
Instead of passing props through multiple intermediate components, shared data is stored in a context and accessed directly by the components that need it.

## 🎯 Objective

Understand what props drilling is and why it is problematic

Learn how Context API solves props drilling

Share data globally without manually passing props

Identify components that no longer act as middlemen

## 🧩 Component Structure

Component1

 └── Component2
 
     └── Component3
     
         └── Component4 
         
             └── Component5
             
                 └── Component6

## 🗂 Folder Structure

src/

 ├── context/
 
 │    └── AppContext.js
 
 ├── components/
 
 │    ├── Component1.jsx
 
 │    ├── Component2.jsx
 
 │    ├── Component3.jsx
 
 │    ├── Component4.jsx
 
 │    ├── Component5.jsx
 
 │    └── Component6.jsx
 
 └── App.js

## 🧠 Context Details
AppContext

Created using createContext

Stores shared values:

a, b, c, d, e, f

Values are defined only once inside the Provider

## 🔍 Component Responsibilities
### Component1

Wraps the entire component tree with AppContext.Provider

Provides values a, b, c, d, e, f

Does not pass props to child components

### Component2

Does not consume context

Does not receive props

Only renders Component3

### Component3

Consumes a and b from context

Displays them using <h4>

### Component4

Consumes c and d from context

Displays them using <h4>

### Component5

Consumes f from context

Displays it using <h4>

### Component6

Consumes e from context

Displays it using <h4>

## 🖥 Output Format

Each value is displayed as:

This is prop a: value


(All values are rendered using <h4> tags)

## ✅ Key Learning Outcomes

Props drilling is eliminated using Context API

Data is accessed directly where needed

Intermediate components remain clean and simple

Proper use of createContext, Provider, and useContext

Ideal use case for global/shared data in React

## 🛠 Technologies Used

React

JavaScript (ES6)

Context API

Functional Components

Hooks (useContext)

## 📌 Conclusion

This project clearly shows how Context API improves code readability, scalability, and maintainability by removing unnecessary prop passing in deeply nested component trees.
