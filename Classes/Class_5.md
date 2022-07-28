## Thinking in React


1. What is the single responsibility principle and how does it apply to components?

   a component should ideally only do one thing. If it ends up growing, it should be decomposed into smaller subcontinents.

2.  What does it mean to build a ‘static’ version of your application?

    It is the easiest way is to build a version that takes your data model and renders the UI but has no interactivity. It’s best to decouple these processes because building a static version requires a lot of typing and no thinking, and adding interactivity requires a lot of thinking and not a lot of typing.

3. Once you have a static application, what do you need to add?
    
    

    Think of all the pieces of data in our example application. We have:

* The original list of products
* The search text the user has entered
* The value of the checkbox
* The filtered list of products


    
4. What are the three questions you can ask to determine if something is state?



    `a.` Is it passed in from a parent via props? If so, it probably isn’t state.

    `b.` Does it remain unchanged over time? If so, it probably isn’t state.

    `c.` Can you compute it based on any other state or props in your component? If so, it isn’t state.


5. How can you identify where state needs to live?

For each piece of state in your application:

* Identify every component that renders something based on that state.
* Find a common owner component (a single component above all the components that need the state in the hierarchy).
* Either the common owner or another component higher up in the hierarchy should own the state.
* If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component.


## higher-order functions



1.  What is a “higher-order function”?


    Functions that operate on other functions, either by taking them as arguments or by returning them, are called 

2. Explore the greaterThan function as defined in the reading. In your own words, what is line 2 of this function doing?

    it will return boolean value, it will compare the new value entered with the value saved in the lower order function

3. Explain how either map or reduce operates, with regards to higher-order functions.

    map or reduce are higher order functions, the either save or compare values or do logic on them, and to do that they make sub functions and deal with the values as that.
