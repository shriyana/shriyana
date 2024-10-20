---
title: Let's Start learning React  
linktitle: React 
toc: true
type: docs
date: "2019-05-05T00:00:00+01:00"
draft: false
menu:
  webbasics:
    parent: The Fundamentals
    weight: 4

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 4
---

ReactJS is a popular JavaScript library for building user interfaces, particularly for single-page applications where data changes over time. It was developed by Facebook and is maintained by Facebook and a community of individual developers and companies.

## What is ReactJS?

ReactJS allows developers to create large web applications that can update and render efficiently in response to data changes. It simplifies the development process by using a component-based architecture.

### Basic Concepts

- **Components**: The building blocks of a React application. Each component is a self-contained module that renders some output.
- **JSX**: A syntax extension for JavaScript that allows you to write HTML directly within React code.
- **State**: An object that determines how a component renders and behaves.
- **Props**: Short for properties, props are read-only attributes passed to components.

### Example

```jsx
import React from 'react';
import ReactDOM from 'react-dom';

function App() {
  return <h1>Hello, React!</h1>;
}

ReactDOM.render(<App />, document.getElementById('root'));
```

## Components

Components are the heart of React. They can be class-based or function-based.

### Function Components

Function components are simple JavaScript functions that return JSX.

```jsx
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}
```

### Class Components

Class components are ES6 classes that extend from `React.Component` and must have a `render` method.

```jsx
class Welcome extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}
```

## JSX

JSX stands for JavaScript XML. It allows you to write HTML elements in JavaScript and place them in the DOM.

### Example

```jsx
const element = <h1>Hello, world!</h1>;
```

### Embedding Expressions in JSX

You can embed any JavaScript expression in JSX by wrapping it in curly braces.

```jsx
const name = 'John';
const element = <h1>Hello, {name}</h1>;
```

## Props

Props are arguments passed into React components. Props are passed to components via HTML attributes.

### Example

```jsx
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}

const element = <Welcome name="Sara" />;
```

## State

State is a built-in object that allows components to create and manage their own data.

### Using State in Class Components

```jsx
class Clock extends React.Component {
  constructor(props) {
    super(props);
    this.state = { date: new Date() };
  }

  componentDidMount() {
    this.timerID = setInterval(() => this.tick(), 1000);
  }

  componentWillUnmount() {
    clearInterval(this.timerID);
  }

  tick() {
    this.setState({
      date: new Date(),
    });
  }

  render() {
    return (
      <div>
        <h1>Hello, world!</h1>
        <h2>It is {this.state.date.toLocaleTimeString()}.</h2>
      </div>
    );
  }
}
```

### Using State in Function Components with Hooks

React Hooks are functions that let you use state and other React features in function components.

```jsx
import React, { useState, useEffect } from 'react';

function Clock() {
  const [date, setDate] = useState(new Date());

  useEffect(() => {
    const timerID = setInterval(() => tick(), 1000);
    return () => clearInterval(timerID);
  }, []);

  function tick() {
    setDate(new Date());
  }

  return (
    <div>
      <h1>Hello, world!</h1>
      <h2>It is {date.toLocaleTimeString()}.</h2>
    </div>
  );
}
```

## Handling Events

Handling events with React elements is very similar to handling events on DOM elements. However, there are some syntax differences:

- React events are named using camelCase, rather than lowercase.
- With JSX, you pass a function as the event handler, rather than a string.

### Example

```jsx
class Toggle extends React.Component {
  constructor(props) {
    super(props);
    this.state = { isToggleOn: true };

    // This binding is necessary to make `this` work in the callback
    this.handleClick = this.handleClick.bind(this);
  }

  handleClick() {
    this.setState((state) => ({
      isToggleOn: !state.isToggleOn,
    }));
  }

  render() {
    return (
      <button onClick={this.handleClick}>
        {this.state.isToggleOn ? 'ON' : 'OFF'}
      </button>
    );
  }
}
```

## Conditional Rendering

In React, you can create distinct components that encapsulate behavior you need. Then, you can render only some of them, depending on the state of your application.

### Example

```jsx
function Greeting(props) {
  const isLoggedIn = props.isLoggedIn;
  if (isLoggedIn) {
    return <h1>Welcome back!</h1>;
  }
  return <h1>Please sign up.</h1>;
}

ReactDOM.render(
  // Try changing to isLoggedIn={true}:
  <Greeting isLoggedIn={false} />,
  document.getElementById('root')
);
```

## Lists and Keys

You can build collections of elements and include them in JSX using curly braces `{}`.

### Example

```jsx
function NumberList(props) {
  const numbers = props.numbers;
  const listItems = numbers.map((number) =>
    <li key={number.toString()}>
      {number}
    </li>
  );
  return (
    <ul>{listItems}</ul>
  );
}

const numbers = [1, 2, 3, 4, 5];
ReactDOM.render(
  <NumberList numbers={numbers} />,
  document.getElementById('root')
);
```

## Forms

Forms in React are similar to HTML forms but require event handling for form submission and input field changes.

### Example

```jsx
class NameForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = { value: '' };

    this.handleChange = this.handleChange.bind(this);
    this.handleSubmit = this.handleSubmit.bind(this);
  }

  handleChange(event) {
    this.setState({ value: event.target.value });
  }

  handleSubmit(event) {
    alert('A name was submitted: ' + this.state.value);
    event.preventDefault();
  }

  render() {
    return (
      <form onSubmit={this.handleSubmit}>
        <label>
          Name:
          <input type="text" value={this.state.value} onChange={this.handleChange} />
        </label>
        <button type="submit">Submit</button>
      </form>
    );
  }
}
```

## Lifting State Up

Often, several components need to reflect the same changing data. The common approach is to lift the shared state up to the closest common ancestor.

### Example

```jsx
class Calculator extends React.Component {
  constructor(props) {
    super(props);
    this.state = { temperature: '' };

    this.handleChange = this.handleChange.bind(this);
  }

  handleChange(e) {
    this.setState({ temperature: e.target.value });
  }

  render() {
    const temperature = this.state.temperature;
    return (
      <div>
        <TemperatureInput
          temperature={temperature}
          onTemperatureChange={this.handleChange} />
      </div>
    );
  }
}

class TemperatureInput extends React.Component {
  constructor(props) {
    super(props);
    this.handleChange = this.handleChange.bind(this);
  }

  handleChange(e) {
    this.props.onTemperatureChange(e.target.value);
  }

  render() {
    const temperature = this.props.temperature;
    return (
      <fieldset>
        <legend>Enter temperature in Celsius:</legend>
        <input
          value={temperature}
          onChange={this.handleChange} />
      </fieldset>
    );
  }
}
```

## Summary

ReactJS is a powerful library for building dynamic and interactive user interfaces. Understanding components, JSX, props, state, event handling, conditional rendering, lists and keys, forms, and lifting state up is essential for creating robust React applications.

## Quiz

### 1. What is a component in React?
- [ ] A JavaScript function or class that optionally accepts inputs and returns a React element.
- [ ] A special HTML element.
- [ ] A CSS class.
- [ ] A type of variable.

### 2. How do you create a class component in React?
- [ ] By defining a class that extends `React.Component` and implementing a `render` method.
- [ ] By using a function that returns JSX.
- [ ] By creating an HTML element.
- [ ] By defining a variable that holds a function.

### 3. What is JSX?
- [ ] A syntax extension for JavaScript that allows you to write HTML directly within React code.
- [ ] A type of JSON file.
- [ ] A new version of CSS.
- [ ] A built-in JavaScript function.

### 4. How do you pass data to a component in React?
- [ ] By using state.
- [ ] By using props.
- [ ] By using classes.
- [ ] By using events.

### 5. What is the purpose of the `setState` function?
- [ ] To update the state object and re-render the component.
- [ ] To change the props of a component.
- [ ] To bind event handlers.
- [ ] To initialize a component.



### 6. Which hook is used to handle side effects in function components?
- [ ] `useState`
- [ ] `useEffect`
- [ ] `useContext`
- [ ] `useReducer`

### 7. How do you handle events in React?
- [ ] By using camelCase event handlers and passing functions as the event handler.
- [ ] By using lowercase event handlers.
- [ ] By calling a function directly within HTML.
- [ ] By using the `handleEvent` function.

Complete this quiz to test your understanding of ReactJS fundamentals!
