
# State and Props

## React lifecycle


### 1. Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?
<br>


*Render phase happens first.*
<br><br>

### 2. What is the very first thing to happen in the lifecycle of React?
<br>

Mounting: During the mounting process, an instance of a component is produced and injected into the DOM. 
<br>
<br>

### 3. Put the following things in the order that they happen: componentDidMount, render, constructor, componentWillUnmount, React Updates
<br>

1. constructor
2. render
3. componentDidMount
4. React Updates
5. componentWillUnmount

<br>

### 4. What does componentDidMount do?

<br>

The moment a component is installed, this function is called.
This is the place to put anything that requires a network request to load or that needs to initialize the DOM.
Any subscriptions should be set up using this manner.
Don't forget to unsubscribe in componentWillUnmount if you do that (). 

<br>
<br>

## React State Vs Props
<br>
1. What types of things can you pass in the props?
   <br>
   props is like arguments to  a function, when we create a component inside a react, we pass the props we want to render.  <br><br>
2. What is the big difference between props and state?

<br>

we pass props into a component and we can't update them inside the components, and state is handled and can be updated inside of that component.
<br><br>
3. When do we re-render our application? <br>

<br>
when we change the state inside our application.
<br><br>
4. What are some examples of things that we could store in state?<br><br>
we store things that we can updated, and our app rerender depends on this data, example for this is inside a form, so we store what user updates.