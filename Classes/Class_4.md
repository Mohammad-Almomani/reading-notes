# React and Forms
    
## React Docs
    
1. What is a ‘Controlled Component’?
    
    it is a technique used to handle the submission by the component's state 

2. Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.


    the default for this, is that the state changes with every key input, we can keep it as that or change it depending on what we want to do, for example if we want to filter images, it's good to have it change on keystroke, but if we want to search for some word or like that, make it search after finish typing.


3. How do we target what the user is entering if we have an event handler on an input field?

    we use handleChange function on the onChange on the select element this.state.value


## Ternary Operator 


1. Why would we use a ternary operator?

    we use it to make the code cleaner and more organized, it is almost the same as if condition


2. Rewrite the following statement using a ternary statement:

    >if(x===y){
      console.log(true);
    } else {
      console.log(false);
    }

    will be:

    >(x===y)?console.log(true):console.log(false;)