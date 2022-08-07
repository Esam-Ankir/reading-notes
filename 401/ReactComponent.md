# Reading: Component Based UI

## react hello world

1.	What are the building blocks of a React app?

 the building blocks of React apps: elements and components. 

2. What is the difference between an element and a React component?
   
***React Element:*** 

It is the basic building block in a react application, it is an object representation of a virtual DOM node. React Element contains both type and property. It may contain other Elements in its props. React Element does not have any methods, making it light and faster to render than components.


import React from 'react';

import ReactDOM from 'react-dom';

  // With JSX 

const ele1 =<h1>Welcome</h1>;

  // Without JSX

const ele1 = React.createElement('h1',{id:'header'},'Welcome');

// Simple javaScript to get the div with id ="root"

ReactDOM.render(ele1,document.getElementById("root")); 

***React Component:*** 

It is independent and reusable. It returns the virtual DOM of the element. One may or may not pass any parameter while creating a component. A component can be further described into functional components and class components.

Note: Always start the components name with the capital letter, react consider the lowercase component name as HTML tags so it will not show the component.


import React from 'react';

import ReactDOM from 'react-dom';
  
function Welcome(user){

return <div>

  <h3>Welcome {user.name}</h3>

</div>

}

const ele = <Welcome name="Guest"/>

ReactDOM.render(ele,document.getElementById("root"));


3.	What are some advantages of React’s component based architecture?


1.	Code Re-usability

2.	Fast Development

3.	Consistency

4.	Maintainability 


## introducing JSX

1.	What is JSX and why do we use it?

***JSX (JavaScript Syntax Extension or JavaScript XML)*** 

is an extension to JavaScript. It provides an easier way to create UI components in React.

There are several reasons why JSX is a good idea:

**It has a low barrier to entry.** JSX is as close to plain HTML and CSS as it currently gets. With JSX, you can easily embed pieces of JavaScript in your templates without having to learn an additional templating language and having to deal with complex levels of abstraction. Any person familiar with HTML, CSS, and JavaScript should have no problem reading and understanding JSX templates.

**TypeScript support.** TypeScript supports the compilation of TSX files with type-checking. This means that, if you make a mistake in the name of an element or an attribute type, the compilation will fail and you’ll see an error message pointing to your mistake. Popular IDEs such as VS Code also support TSX files and provide code-completion, refactoring, and other useful features.

**Security.** JSX takes care of the usual output sanitization issues to prevent attacks such as cross-site scripting.

2.	Describe the process of embedding JavaScript expressions in JSX.


function formatName(user) {

  return user.firstName + ' ' + user.lastName;

}


const user = {

  firstName: 'Harper',

  lastName: 'Perez'

};


const element = (

  <h1>

    Hello, {formatName(user)}!

  </h1>

);


3.	Is it safe to embed user input in JSX? Explain.

It is safe to embed user input in JSX:

const title = response.potentiallyMaliciousInput;

// This is safe:

const element = <h1>{title}</h1>;

By default, React DOM escapes any values embedded in JSX before rendering them. Thus it ensures that you can never inject anything that’s not explicitly written in your application. Everything is converted to a string before being rendered. This helps prevent XSS (cross-site-scripting) attacks.


## rendering elements

1.	Explain what a React Component is to a non-technical friend.

 React is based upon component design. Everything in React is a component which makes it easy to reuse components frequently.

You can compare components with lego blocks. We use them as building blocks to build a bigger and meaningful application.


2.	Describe mutability and React Components, specifically, how is the UI updated?

React elements are immutable. Once you create an element, you can’t change its children or attributes. An element is like a single frame in a movie: it represents the UI at a certain point in time.


3.	If changes are made to the UI, what does React update?

With our knowledge so far, the only way to update the UI is to create a new element, and pass it to root.render().

