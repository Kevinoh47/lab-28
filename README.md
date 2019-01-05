![CF](http://i.imgur.com/7v5ASc8.png) LAB
=================================================

## Lab 28 Props and State

### Author: Kevin O'Halloran

### Links and Resources
* [repo](https://github.com/Kevinoh47/lab-28)
* [assignment1-props-sandbox](https://codesandbox.io/s/ykjljx4zkj)
* [assignment2-internal-state-sandbox](https://codesandbox.io/s/ox8o9l89jz)
* [assignment3-external-state-sandbox](https://codesandbox.io/s/132851l9nq)

### Assignment 1 (Props Practice) Modules
#### `app.js`
##### Exported Values and Methods
class App exports itself. It has a state object with several values that are used to pass down as props to the child Message component. It contains a render method which is used to compose and render the react application page.

#### `clock.js`
##### Exported Values and Methods
Clock is a functional component that exports itself. This component returns a formatted date string.


#### `index.js`
##### Exported Values and Methods
The index.js is the main file of the React application, rendering the App component in the rootElement.

#### `message.js`
##### Exported Values and Methods
The Message class component includes a constructor with state for text. It has a render method which renders the message text received via props, as well as other values received from props. This component exports itself.

#### `todaysDate.js`
##### Exported Values and Methods
TodaysDate is a functional component that exports itself. This component returns a formatted time string.


### Assignment 2 (Internal State Practice) Modules
#### `counter-form.js`
##### Exported Values and Methods
The CounterForm class exports itself. It contains a constructor, with a state object. It contains three methods: 

###### handleChange(event)
Thi handleChange method fires on every change to the form, and is used to capture any form field updates and update any corresponding state properties. In this form, those state properties are used to populate headers in real time.

###### handleSubmit(event)
The handleSubmit method is used to manage the state counter property on form submit.

###### render()
The render method builds the form, using state to deliver headers as well as as the counter value.

#### `index.js`
##### Exported Values and Methods
The index.js is the main file of the React application, rendering the App component in the rootElement.


### Assignment 3 (External State Practice) Modules
In this assignment, we practice pushing functions down from parent components to child components, where they are executed and the results are returned to the parent to render.

#### `app.js`
##### Exported Values and Methods
The App component is the main component, and exports itself. It contains a state object, and imports child components. 
It contains the following methods:

###### handleName(data)
The handleName function is passed down to the child NameForm component, which will gather form data and pass it back to the parent so that the parent state can be updated.

###### updateCount()
Similarly, the updateCount method is passed to the Content component. It is used to manage the Counter state when the form is submitted.

###### fetchPeople() 
The fetchPeople method is likewise passed to the Content component. It executes an API call and sets the people state array with the values returned by the API.

###### render()
The render method composes and renders the React web page.


#### `content.js`
##### Exported Values and Methods
The Content class exports itself. It is a child component. It contains a render method that builds a React Fragment containing buttons that execute the function passed down via props.fetch and props.updateCount. When the method provided by props.fetch is executed back on the parent App component, it then gets the results as props.people, and iterates over that array and renders the list. It also renders the counter, whose value it receives back from the parent App as props.count. 

#### `form.js`
##### Exported Values and Methods
This file creates the NameForm component. Using the handeNameChange event handler locally, it sets the name state as the form is updated. This is used to update headers in real time. Using the handleSubmit event handler, again locally, it updates a variable called formData with a copy of the local state object, and then passes this back to the parent App component as the input variable for the updateName function, which was passed down from the parent App component. On form submit the updateName function is executed by App and updates the name value in the App component.

#### `index.js`
##### Exported Values and Methods
The index.js is the main file of the React application, rendering the App component in the rootElement.


#### Tests
* How do you run tests?
* What assertions were made?
* What assertions need to be / should be made?

#### UML
Link to an image of the UML for your application and response to events
