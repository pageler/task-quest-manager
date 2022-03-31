# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

## ---------- Notes -------------

-   RoadsideCoder
    <href="https://www.youtube.com/watch?v=uEVHJf30bWI&list=PLKhlp2qtUcSbZaGj7DGyZ7BLupZEZOkAw&index=3">

C:\Users\harak\Documents\ProgWorkshop\MERN>npx create-react-app <project-name> --template typescript

-   Typescript basics

? makes the params of an object optional

Union, <type | different-type>

Function type, printName: (name: string) => void; // returns undefined <br />
Function type, printName: (name: string) => never; // returns unknown

-   Aliases(type and interface)
    interface Object {key: value arguments};
    Examples:
    type Person = {name: string; age: number;}
    interface Person {name: string; age: number;}
    type X = {a: string; b:number;}
    type Y = X & {c: string; d:number;} // Y is extended to X
    interface Person {name: string; age: number;}
    interface Guy extends Person {profession: string}
    type X = Person & {a: string; b: number;}
    interface Person extends X {name: string; age?: number;} // age optional

-   Project Notes
    ./App.tsx
    App: React.FC // React Functional Component

./App.css
.input parent position: relative and child input_submit position: absolute so button is inside the input\_\_box

./model.ts // normal ts file to reuse properties throughout project

./App.tsx
handleAdd function adds todos to todo list: add to <InputField />; ./InputField.tsx added to interface Props, InputFiled function params

./InputField.tsx
useRef hook to restore background on submit button click; inputRef.current?.blur();

./TodoList.tsx
params todos for todo list, and setTodos for deleting and striking

$ npm install react-icons

./SingleTodo.tsx
<s ... >string</s> strike-through
edit state tracks it the edit id "on" or "off" <boolean>
editTodo state holds the value of the todo <string>
if edit it true display input box, else display todo
useRef hook used to set focus on edit box input upon submit of edit button
useEffect hook contains the logic to set useRef focus
incorporate useReducer into project (./model.ts)

./TodoList.tsx
"todos" are Active Tasks, and "todos remove" are for Completed Tasks

$ npm i react-beautiful-dnd
$ npm i @types/react-beautiful-dnd

./App.tsx
completedTodos, setCompletedTodos state
send to todos component in return ()

./TodoList.tsx
list completedTodos and setCompletedTodos in interface
list completedTodos and setCompletedTodos in function params
list completedTodos and setCompletedTodos in return of component

./App.tsx
wrap return (<div> </div>) with <DragDropContext></DragDropContext> element

./TodoList.tsx
wrap return (for each <div></div>) with <Droppable droppableId="name"></Droppable> element

./SingleTodo.tsx
wrap return (<form></form>) with <Draggable draggableId={todo.id.toString()} index={index}></Draggable> element

## \***\*\*\*\*\*\*\*** TODO **\*\***\*\*\***\*\***

1. Fix todo under lapping Completed Task container
2. Save and restore in localStorage
3. Make image properly responsive
4. Convert to Redux state management
5. Publish project
