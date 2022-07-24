
# Props and Components

Component-based architecture is focused on the breakdown of the design into discrete functional or logical components that represent well defined communication interfaces comprising methods, events, and attributes.

Reusability of components is the main goal of component-based architecture.
A component is a reusable and self-deployable binary unit that contains the functionality and behaviors of a software element.

## Components
<br/><br/>
### 1- What is a “component”?
<br/>
A component is a well-defined, modular, and reusable capability that exports its implementation as a higher-level interface.Also, a component is a piece of software that has one or more capabilities and is designed to interact with other components.
<br/><br/>

### 2-What are the characteristics of a component?
<br/>
Reusability: Typically, components are made to be utilized in several contexts and applications.
However, certain parts might be created for a particular function.

Replaceable: Components can be readily swapped out for others that are comparable.

Not context specific: Components are made to function in a variety of settings and scenarios.

Extensible: To add additional behavior, a component can be extended from an existing component.

Encapsulated: A component only shows the interfaces necessary for the caller to perform its functionality, it conceals information about internal operations, variables, or state.

Independent: Components are made to depend on other components as little as possible.
<br/><br/>

### 3-What are the advantages of using component-based architecture?
<br/>

Ease of deployment: It is simpler to replace older versions as new compatible ones become available without affecting other parts of the system or the system as a whole.

Reduced cost: Spreading the expense of development and maintenance is made possible through the usage of third-party components.

Ease of development: To offer stated functionality, components implement well-known interfaces, enabling development without affecting other system components.

Reusable: Reusable components allow for the distribution of the expense of creation and upkeep over a number of applications or systems.

Modification of technical complexity: Through the usage of a component container and its services, a component alters complexity.

Reliability: Since the reuse of each component improves the dependability of the entire system, the total system reliability rises.

System maintenance and evolution: The implementation is simple to modify and update without having an impact on the rest of the system.

Independent: independent and adaptable component connection. independent component development carried out concurrently by various groups. Productivity in the current and future development of software. 
<br/><br/>

## Props
<br/>

### 1-What is “props” short for?
<br/>
“Props” is a special keyword in React, which stands for properties and is being used for passing data from one component to another.
<br/><br/>

### 2-How are props used in React?
<br/>
A-Define an attribute and its value(data).
B-Then pass it to child component(s) by using Props.
C-Finally, render the Props Data.

note that props are read only, so it cannot be changed by the child components.
<br/><br/>
### 3-What is the flow of props?
<br/>

Step 1: Defining Attribute & Data:


assign attributes and values to HTML tags.


Step 2: Passing Data using Props:

take the attribute you assigned ChildComponent and pass it by using props either to a function ar a react component.

Step 3: Rendering Props Data:
render the props object by using string interpolation.