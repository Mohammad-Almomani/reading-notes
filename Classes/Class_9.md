# Functional Programming


## Functional Programming Concepts

1. What is functional programming?

    Functional programming is a programming paradigm "a style of building the structure and elements of computer programs" that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data 

2. What is a pure function and how do we know if something is a pure function?

    It returns the same result if given the same arguments (it is also referred as deterministic)

    It does not cause any observable side effects, It returns the same result if given the same arguments


3. What are the benefits of a pure function?

    The code’s definitely easier to test. We don’t need to mock anything. So we can unit test pure functions with different contexts:

    Given a parameter A → expect the function to return value B
    Given a parameter C → expect the function to return value D

    A simple example would be a function to receive a collection of numbers and expect it to increment each element of this collection.

4. What is immutability?

     its state cannot change after it’s created. 

5. What is Referential transparency?

    Basically, if a function consistently yields the same result for the same input, it is referentially transparent.

    >pure functions + immutable data = referential transparency


## Node JS Tutorial


1. What is a module?

    Module is just essentially another javascript file.

2. What does the word ‘require’ do?

    To use module functionality elsewhere  in the application.

3. How do we bring another module into the file the we are working in?

    we use require then the module path in side ("").

4. What do we have to do to make a module available?

    we export the module then import it where do we want to work on it.