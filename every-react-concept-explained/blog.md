React is a JavaScript library that allows you to develop front-end code in minutes. It has prebuilt methods and functions to perform certain tasks. React as a library includes complex terms like reconciliation, bundlers, props, etc. What do they actually mean?

In this article, you will learn about this exaggerated concept more simply.

## 1. **Components**

Components are small bit of reusable code that return a React element to be rendered on a webpage. It is a group of code that make up a single part of the webpage like buttons, navbar, cards, etc. It is just like a JavaScript function but returns a rendered element. It accepts parameters called **"Props"**. Components are named with capital case.

**Example Of Functional Component**

```javascript
function Heading(props) {
  return <h1>Join us, {props.name}!</h1>;
}
```

<div style="background: #e0f7fa; color: #01579b; padding: 20px;">Note:
<ul>
<li style="list-style: circle;">Functional Components are recommeded instead of Class based.</li> <li style="list-style: circle;">Functional components are often called stateless components.</li>
</ul>
</div>

## 2. **JSX**

JSX is JavaScript XML, which allows us to write HTML in React. It introduces XML-like tags and attributes to create React elements. It makes it easy to create React Components by letting you write HTML-like code in `.jsx` files. Instead of using complicated JavaScript, JSX makes the code readable and clean. React DOM uses camelCase for attribute naming such as `htmlFor, onClick`.

**Example of JSX**

```javascript
<h1 className="head">This is H1!</h1>
```

## 3. **Fragments**

Fragments in React allows you to return multiple elements from a component. It groups the list of elements without creating a extra DOM nodes. It cleans all the extra divs from the DOM. This quickly renders the UI.

**Example of Fragments**

```JavaScript
const App = () => {
  return  (
    <>
      <h1>Eat</h1>
      <button>Learn more</button>
      <p>Code is Fun</p>
      <button>Repeat</button>
    </>
  );
}
```

<div style="background: #e0f7fa; color: #01579b; padding: 20px;">Note:
<ul>
<li style="list-style: circle;">Fragments makes the code cleaner and readable.</li> <li style="list-style: circle;">It are memory efficient.</li>
<li style="list-style: circle;">It cannot have CSS styles and Keys.</li> 
</ul>
</div>

## 4. **Props**

"Props" is a special keyword in React that stands for properties. It is used to transfer data between components. The follow of data transfer is uni-directional i.e from parent component to child component.

**Example of Props**

```javascript
function Head(props) {
  return <p>{props.children}</p>;
}
```

<div style="background: #e0f7fa; color: #01579b; padding: 20px;">
Note: Props is read-only, which ensures that child components don't manipulate the value coming from parent component.
</div>

## 5. **State**

Components need to keep track of certain values when user interacts. Let's say the light/dark mode theme toggle button changes its value(from light to dark & vice versa) when a user clicks on the button. Components need to remember the current value of theme. In React, this kind of component-specific memory is called state.

State is defined using a `useState()` hook; more on that later.

**Example of defining state**

```javaScript
const [index, setIndex] = useState(0)
```

<div style="background: #e0f7fa; color: #01579b; padding: 20px;">
Note: It's always a good practice to define state in a top-level component to share it easily with other child components and ensure a single source of truth.
</div>

## 6. **Lifecycle Methods**

Lifecycle methods are special functions you can use within React classes to perform actions at various stages of a component's existence. These stages are:

- Mounting: When a component is first created and inserted into the DOM.
- Updating: When a component's props or state change, causing the component to re-render.
- Unmounting: When a component is removed from the DOM.

## 7. **Purity**

Purity in functional programming is when a given same input returns the same output. The inputs is the only factor that determine the ouput then the function is said to be pure.

In React a component is said to be pure when it returns the same ouput for the same input (viz props)

## 8. **Strict Mode**

Strict Mode is a developmental feature in react that enables extra safety features to improve code quality. It shows warnings regarding potential errors and bugs into the code. It logs warning into the browser's console.

**Example of Strict Mode**

```JavaScript
import { StrictMode } from 'react';

function App() {
  return (
    <>
     <StrictMode>
        <Header />
        <Sidebar />
        <Content />
        <Footer />
     </StrictMode>
    </>
  )
}
```

![Images](Strict Mode in React Showing Browser Console)

## 9. **Hooks**

Hooks in React allows to use state and other React features without writing class components. Hooks are functions that provide access to React's state management, side effects, and other features.

Some commonly used hooks: `useState`, `useMemo`, `useRef`, etc.

**Example of Hooks**

```javaScript
import React, { useState } from "react"; // Importing useState hook;

function FavoriteColor() {
  const [color, setColor] = useState("red"); // Initializing the state and setter function;

  return (
    <>
      <h1>My favorite color is {color}!</h1>
      <button
        type="button"
        onClick={() => setColor("blue")} // Updating the state;
        >Blue</button>
      <button
        type="button"
        onClick={() => setColor("red")} // Updating the state;
      >Red</button>
      <button
        type="button"
        onClick={() => setColor("yellow")} // Updating the state;
      >Yellow</button>
      </>
  );
}
```

<div style="background: #e0f7fa; color: #01579b; padding: 20px;">Note:
<ul style="list-style: circle;">
<li>Hooks can only be called inside React function components.</li>
<li>Hooks can only be called at the top level of a component.</li>
<li>Hooks cannot be conditional.</li>
  </ul>
</div>

## 10. **Context API**

The Context API is used to share data like state, functions across the component tree without passing props down manually at every level. It avoids _prop drilling_ by simplifying state management and sharing data across the component. With Context API the data is shared directly with the child component who will consume it.

The `useContext()` method is used to create a context. This function returns a context object with two components – a `Provider` and a `Consumer`.

The `Provider` is used to wrap the part of your component tree where you want the context to be available. It accepts a compulsory value prop that holds the data you want to share across other components.

The `useContext` hook is used to access the data.

**Example of Context API**

Create a context using `createContext()` method. Wrap child components in the Context Provider and supply the state value.

```javaScript
import { useState, createContext} from "react";

const UserContext = createContext();

function ParentCounter() {
  const [count, setCount] = useState(10);

  return (
    <UserContext.Provider value={count}>
      <h1>{`Current Count: ${count}!`}</h1>
      <Button />
    </UserContext.Provider>
  );
}
```

Use `useContext` hook to access the value of age.

```javaScript
import { useContext } from "react";

function GrandChildConsumer() {
  const age = useContext(UserContext);

  return (
    <>
      <h1>This is GrandChildConsumer</h1>
      <h2>{`Current Count: ${count}`}</h2>
    </>
  );
}
```

<div style="background: #e0f7fa; color: #01579b; padding: 20px;">Note: The `useContext` hook is often used instead of Consumer for better readability and simplicity.
</div>

## 11. **Lists and Keys**

A `Key` is a special kind of attribute for list items in React. It acts as a unique identifier for each items when it is updated, deleted, or added.

Assigning index of the item as the `Key` is discouraged because if the items are rearranged it will affect the expected behaviour.

Imagine in shopping cart you have 10 items added and each item have a unique index as a `Key`. Now, you decide to remove the first and fifth item from the cart. When the items are removed the indexing will change; the second item will become first and sixth item will become fifth item.

**Example of Lists and Keys**

```javaScript
const fruits = ["apple", "banana", "orange"];

function FruitList() {
  return (
    <ul>
      {fruits.map((fruit, index) => (
        <li key={index}> {fruit} </li>
      ))}
    </ul>
  );
}


```

<div style="background: #e0f7fa; color: #01579b; padding: 20px;">Note:
<ul>
<li style="list-style: circle;">It is recommended to use string as a `Key` that uniquiely identifies the item in the list.</li> <li style="list-style: circle;">Third-party libraries like UUID offer the functionality to create unique keys.</li>
</ul>
</div>

## 12. **Form: Controlled & Uncontrolled Components**

React forms allows to collect and manage user input better than traditional HTML form. These forms are built using components and store the user inputs into state. There are two types of components:

### Controlled Components

In Controlled components, the form's state is managed by the component himself. This is the recommended approach for managing form data in React. When the user interacts with the form (e.g., typing in an input field), the component's state is updated to reflect the changes.

**Example of Controlled Component**

```javaScript
function ControlledInput() {
  const [name, setName] = useState('');

  const handleChange = (e) => {
    setName(e.target.value);
  }

  return (
    <div>
      <label htmlFor="name">Name: </label>
      <input type="text" id="name" value={name} onChange={handleChange} />
      <p>Your name is: {name}</p>
    </div>
  );
}
```

### Uncontrolled Components

Uncontrolled components rely on the DOM to manage the form data. The component doesn't directly control the form's state, but it can access the values using DOM methods like ref.

**Example of Uncontrolled Component**

```javaScript
function UncontrolledInput() {
  const nameRef = useRef(null);

  const handleClick = () => {
    console.log(nameRef.current.value);
  }

  return (
    <div>
      <label htmlFor="name">Name: </label>
      <input type="text" id="name" ref={nameRef} />
      <button onClick={handleClick}>Get Name</button>
    </div>
  );
}
```

<div style="background: #e0f7fa; color: #01579b; padding: 20px;">Note:
<ul>
<li style="list-style: circle;">Controlled components provides form validation because the user's input is instantly reflected due to use of state.</li> <li style="list-style: circle;">Form validation is not possible in uncontrolled components because the user's input can only be accessed after the form is submitted.</li>
</ul>
</div>

## 13. **React Router**

- Introduction to React Router for navigation
- Basic setup and usage
- Example: Creating routes and navigating between pages

React Router is a standard library for routing in React. It enables navigation among various components in the React app. It allows changing the browser URL and syncing the UI with the URL. React Router is important for creating single-page applications (SPA) with navigation features.

First, you need to install React Router from your terminal.

**Installing React Router**

```bash
# If you are using npm
npm install react-router-dom

# If you are using yarn
yarn add react-router-dom
```

**Example of React Router**

```JavaScript
import { BrowserRouter, Routes, Route } from "react-router-dom";
import Home from "./pages/Home";
import About from "./pages/About";
import Contact from "./pages/Contact";
import NoPage from "./pages/NoPage";

export default function App() {
  return (
    <BrowserRouter>
      <Routes>
          <Route path="/" element={<Home />} />
          <Route path="about" element={<About />} />
          <Route path="contact" element={<Contact />} />
          <Route path="*" element={<NoPage />} />
      </Routes>
    </BrowserRouter>
  );
}
```

First wrap your content into the `<BrowserRouter>`. Then we define `<Routes>` and inside that introduces the `<Route>` for navigation. `<Route>` has `path` which specifies URL of the page and `element` attribute which specifies the component that needs to be rendered on the defined path.

<div style="background: #e0f7fa; color: #01579b; padding: 20px;">Note:
<ul>
<li style="list-style: circle;">An app can have multiple < Routes >.</li> <li style="list-style: circle;">< Route > can be nested.</li>
<li style="list-style: circle;">`react-router-dom` also has < Link > and < Outlet > Component for navigation.</li>
</ul>
</div>

## Conclusion

The best way to learn any programming language is to practice more projects. Build small projects and experiment with the concepts.

You can also stay connected with me by following me here and on [X](https://twitter.com/JiitendraC), [GitHub](https://github.com/J11tendra/), and [LinkedIn](https://www.linkedin.com/in/jiitendrachoudhary/).
