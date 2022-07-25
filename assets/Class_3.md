# Passing Functions as Props


## Reading

### React Docs
1. What does .map() return?

    map returns an array

2. If I want to loop through an array and display each value in JSX, how do I do that in React?

    Step 1: declare a variable and use 'require('your jsx file path')' as its value

    step 2: map through the array in the return section to render it

3. Each list item needs a unique `key`.
   
4. What is the purpose of a key?

    Keys help React _identify which items have changed_, are added, or are removed.



### The Spread Operator


1. What is the spread operator?

    it is a quick syntax for adding items to arrays, combining arrays or objects, and spreading an array out into a function’s arguments.
    
    `Example: `

  >  function sum(x, y, z) {
    return x + y + z;
    }

    const numbers = [1, 2, 3];

    console.log(sum(...numbers));
     expected output: 6

2. List 4 things that the spread operator can do.

- Copying an array
- Using an array as arguments
- Adding an item to a list
- Adding to state in React

3. Give an example of using the spread operator to combine two arrays.

   `Example: `

  >  function sum(x, y, z) {
    return x + y + z;
    }

    const evenNumbers = [2, 4, 6];
    const oddNumbers  = [1, 3, 5];

    let combineNumbers = {...evenNumbers,...oddNumbers}
     expected output: {evenNumbers: [2, 4, 6], oddNumbers: [1, 3, 5]}

4. Give an example of using the spread operator to add a new item to an array.
    >const fruits = ['🍏','🍊','🍌','🍉','🍍']          
const moreFruits = [...fruits];     
console.log(moreFruits) // Array(5) [ "🍏", "🍊", "🍌", "🍉", "🍍" ]        
console.log(...[...fruits,'...',...moreFruits]) //  🍑 🍊 🍌 🍉 🍍 ... 🍏 🍊 🍌 🍉 🍍

5. Give an example of using the spread operator to combine two objects into one.

 >var a = {
  1: {
    687: {
      name:'test1'
    }}}     
var b = {
  1: {
    689: {
      name:'test2'
    }
  }
}       
var c = {
  ...a,
  ...b
}           
expected output 
{
  "1": {
    "689": {
      "name": "test2"
    }
  }
}


## Videos


1- In the video, what is the first step that the developer does to pass functions between components?

 create a function 'increment' where the state he want to change is in 

2- In your own words, what does the increment function do?

when ever you you press on the button or what ever you attached to the listener you added, the count will increase by one

3- How can you pass a method from a parent component into a child component?


call it on the element you want to use it on, like button, example \<button onclick="this.increment">


4- How does the child component invoke a method that was passed to it from a parent component?

when you click on the element attached to the method, for example in the video it was a button, another example is when you press on a photo