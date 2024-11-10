Section Overview:
  1) The best place to learn something is often the official documentation.
  2) How to architect and build the app.

Environment Setup For Mac:
  1) Yarn is simply another package manager.
    - Made by Facebook when NPM was having issues.
  2) NPM is perfectly stable now.
  3) You should not use both NPM and Yarn in the same folder.

NPM vs YARN:
  1) Install dependencies from package.json: 
    - npm install == yarn
  2) Install a package and add to package.json: 
    - npm install package --save == yarn add package
  3) Install a devDependency to package.json: 
    - npm install package --save-dev == yarn add package --dev
  4) Remove a dependency from package.json: 
    - npm uninstall package --save == yarn remove package
  5) Upgrade a package to its latest version: 
    - npm update --save == yarn upgrade
  6) Install a package globally: 
    - npm install package -g == yarn global add package

Create React App - NPX:
  1) NPX is a tool that gets included within NPM.
  2) NPM coordinate and leverage packages we download.
  3) NPX installs and executes immediately and gets deleted right after.

Create React App - React-Scripts 1:
  1) package.json writes what the dependencies of this app are.
  2) React is the underlying engine that runs how the applications get built.
  3) ReactDOM specifies the engine that should be directed towards web related applications.
  4) Entry point for every project is the index.js file.
  5) <App /> is the entire application.
  6) Everything lives inside what is being rendered.

Create React App - React-Scripts 2:
  1) When we deploy our code it needs to be optimized and to be efficiently small. Internet connection varies and can be slow.
  2) npm build: 
    - React will generate an optimal build for us.
    - Different browsers consume the code slightly differently.
    - Main 2 packages: Babel and Webpack
      - Babel changes our code to older JS to make it easier for all browsers to understand.
      - Webpack: Modularizes our code. Module being a chunk. Optimize our code for better user experience.
      - You can modify them to follow specify rules that you want.
  3) npm test: Ways for us to make sure the code does what we expect it to.
  4) npm eject:
    - Most of the time you don't need to use this.
  5) manifest.json file:
    - Used for progressive web app.
    - For people to download to access offline.
      - Use your application not through the browser.

Create React App - Everything Else:
  1) App.js represents our entire React application.
  2) React is using functions to return HTML.
  3) A component is a self-contained representations of a combination of HTML, CSS and JS.
  4) Allows us to build UI in a efficient, componentized way.  

Don't Eject:
  1) By usign create-react-app we automatically get the best system and project build out of the box therefore npm eject is very rarely needed and even used.

Monsters Rolodex - Class Components:
  1) A great React developer knows when React is rendering or re-rendering your website.
  2) Write things in either class or functional components with hooks.
  3) Functional components with hooks the more modern way.
  4) JSX: 
    - A syntax extension of JS.
    - Extended the functionality of JS.
    - Write what looks like HTML but really closely resembles.
  5) Class component allows us to tell React what we expect it to render and how we expect it to render things.
  6) Class component allows us to tell explicitly what we want to render.

Monsters Rolodex - Component State:
  1) Local state is some information that only this component is aware of and can modify.
  2) The way to access the state is through constructors method.
  3) Super calls underlying constructor method of other classes extending from.
  4) this.state is always a JSON object.
  5) Access a JS variables using {}. You want to give it a key value pair.
  6) When variables change, React will re-render the information that represents the UI.

 Monsters Rolodex - setState:
  1) React allows to bind event handlers to any HTML tags.
  2) React determines when to re-render is when state is a completely different object in memory.
  3) Function or callback function: Call handlers during some process.
  4) React will only re-render when state is a completely different object in memory.
  4) Shallow merge: Shallow Merging means it only cares about the first level of the object and will replace anything deeper than the first level.
  4) setState updates the state to a different object.
    - React sees this as a different object in memory, the component is re-rendered.

Monsters Rolodex - States and Shallow Merge:
  1) Shallow merge only updates the keys for the values that are being passed to it.
  2) Shallow merge doesn't care the history or how it looked like.
  3) Best practice: Make sure that when we update our state always use the same types of values.
  4) Set state should pass it a function is better. (Will be explained later)

Monsters Rolodex - setstate and Secondary Callback:
  1) setState is an asynchronous call.
    - setState has 2 arguments, first one is an updater function, second one is a callback function.
    - Callback functions will only run after the first function is completed.
  2) If we pass a function to setState,we get access to state and props.
  3) Props is something to do with components.
  4) Callback function is entirely optional but ideal optimal way to write setState.
  

Monsters Rolodex - Mapping Arrays to Elements:
  1) We can reuse the same HTML template using map.
  2) A good rule of thumb as to when to use the key attribute you saw in the previous video, is this: Anytime you use the map() function inside of render, or you have a list of the same jsx elements one after another, they need a key attribute.

Monsters Rolodex - Keys for Mapping:
  1) A key property is the element html that we're returning from our map.
  2) ID is the unique value most of the time.
  3) Why do we need the key value? Due to React and re-rendering.
    - Make it more optimized and efficient.
    - To differentiate between each item.
  4) React is the only thing that needs key values.

Monsters Rolodex - Single Page Applications (SPAs):
  1) With React, no need to go to server for the code when we navigate and change pages.
  2) Not entirely true when we do customized optimizations.

Monsters Rolodex - Lifecycle Method: componentDidMount:
  1) Where we're going to leverage the actual array once we get it inside our component.
  2) Application should not have to worry about what data looks like.
  3) We need to know what will be the empty (aka null) case.
  4) When do I get the list? How do I get the list? Where do I put the list?
  5) We want to get the API the moment it's rendered (aka mounted) by React.
  6) Mounting is the first time a component gets placed onto the DOM.
  7) What we fetch we want it in a JSON format.
  8) A Promise is asynchronous.

Monsters Rolodex - Renders & Re-renders:
  1) Constructor runs before anything in any class.
  2) In the constructor, initialize the state.
  3) Render runs next and determines what to show.
  4) The lifecycle method will be run next.
  5) Render will run again once the state changes.
    - Key thing: Understand React class components when re-rendering happens.

Monsters Rolodex - Input Search Box Component:
  1) Always work on functionality of the application before working on CSS.
  2) For every html tag there is an equal React component.
  3) Note that some of it is named differently. (Example: class vs className)
  4) We shouldn't access anything starting with an underscore.
    - The main thing we want is 'target'.

Monsters Rolodex - Searching & Filtering:
  1) As a general practice you always want to use non modifying method. aka immutability, is a general best practice.

Monsters Rolodex - Storing Original Data:
  1) We need to keep the original list for future reference.
  2) The best place to keep track of something is in the state.
  3) JS all variables are locally scoped.

Monsters Rolodex - Optimizations:
  1) Anonymous function: A function that is not stored anywhere in a variable.
  2) A function put inside a render is being run every single time.
    - A needless performance risk.
  3) Best to move it out.
  4) Use destructuring instead of using 'this' all the time.
    - More readable.

Monsters Rolodex - Understanding Components:
  1) React ties together the visual representation and the functional representation of UI.
  2) Component aims to tie together reusable portions of the code into one segment.
  3) When you can create a component, you can genericize the functionality.
    - Becomes as reusable as possible.
  4) Ideally it has one single responsibility.

Monsters Rolodex - CardList Component:
  1) In component there can be only one parent level holder HTML tag.
  2) All must be capsulated in one parent component.
  3) Class components are clearer to see.

Monsters Rolodex - Component Props:
  1) Props: Shorthand for properties.
  2) You can pass props from one component into another.

Monsters Rolodex - Rendering and Re-rendering part 2:
  1) Components will re-render when:
    - Props change.
    - setState gets called.
  2) This 2 is how React determines to re-render.
  3) React (Component tree) always renders from top-down.
    - Parent to child components. 
  
Monsters Rolodex - CSS in React:
  1) App.js is the entry point to our entire application.
  2) App.js is not the same category as our other components (not reusable).
  3) CSS styles file applies to the entire website.
    - Need to make sure that the className does not repeat.

Functional vs Class Components:
  1) Functional components utilize hooks.
  2) React started with class components.
  3) They are 2 different styles of writing components.
  4) Most of the time you can use either or.

Class Component Lifecycle Method Breakdown:
  1) 3 phases: Mounting, Updating, Unmounting.
  2) Mounting: Constructor -> render -> DOM Update -> componentDidMount
  3) Updating: New props/setState()/forceUpdate() -> render -> DOM Update -> componentDidUpdate
    - forceUpdate() is not often times to use. Only used when using a third party library that doesn't have React-based library.
    - Most of the time rely on what is provided.
  4) Unmounting: Taking a component off the page. componentWillUnmount.
    - Navigating to different pages or changing your UI.
    - This is done when you need to remove certain things that might affect the performance.
  5) componentDidMount, componentDidUpdate, componentWillUnmount is unique to class components. 
  6) Functional components do not have lifecycle methods, but follow the same three phases/structures of class components.

Monsters Rolodex - Functional Component Intro:
  1) Functional components are pure functions.
    - No constructor, lifecycle method, render().
  2) Runs top to bottom.
  3) Similar to Javascript functions. Takes some arguments (props of this component) and returns JSX.
  4) There are no lifecycles for functional components.
  5) Think in terms of functions and side effects.
  6) 4 ideas to understand: functions, side effects, pure functions, impure functions.

Pure & Impure Functions:
  1) Pure function: Everything inside dictates what it returns.
    - Completely isolated from what get passed into it.
    - Never produces a side effect.
  2) Impure function: function that contains one or more side effects. It mutates data outside of its lexical scope and does not predictably produce the same output for the same input.
  3) React uses impure functions.
    - Use hooks to create impure functions.

Monsters Rolodex - Hooks: useState:
  1) Encapsulate local state in a functional component.
  2) Use array destructuring. useState gives an array of 2 values.
    - [value, setValue]
  3) If you have multiple values from a state, you need multiple useState calls.
  4) Pass in initial value to the searchfield.
  5) It is whatever type when you pass it to the state hook.

Monsters Rolodex - Functional Component Re-rendering:
  1) The way it determines to re-render is the same.
  2) Functional components need to re-run the whole thing every time a state or props change happens.

Monsters Rolodex - Infinite Re-rendering:
  1) It cannot isolate one part of the function it needs to run every line.
  2) Infinite re-rendering happens when each update sees that the value is always pointing to a new object in the memory (Which is the key to trigger re-rendering)
  3) Side effects can be triggered using useEffect hook.
  4) Any fetch call is a side effect.

Monsters Rolodex - Hooks: useEffect:
  1) useEffect hook has 2 arguments:
    - Callback function.
    - Array of dependencies.
      - Most likely to be state values.
  2) Whenever values in the array of dependencies change, it will run the callback function.

Monsters Rolodex - Remaining Components:
  1) React components only get 2 arguments:
    - props
    - forwardRef

React v18: Migrating from React v17 + ReactDOM v18 Changes:
  1) npm upgrade react react-dom --latest
  2) Not the same way as before versions but conceptually is the same.

React v18: Strict Mode Changes:
  1) React.StrictMode enforces we don't use any deprecated methods.
  2) React.StrictMode is double rendering so that it catches weird behaviours.

DOM & Virtual DOM:
  1) In Real DOM, is computationally expensive to make changes.
  2) This process is known as reflow.
  3) React makes a duplicate copy in Javascript, known as Virtual DOM.
  4) With changes, it will make a copy of the Virtual DOM. The original Virtual DOM is known as Snapshot.
  5) The copy will implement the changes.
  6) Compare between the copy and and the snapshot and update the changes to the Real DOM.

React & ReactDOM:
  1) We have been using the easier way with lots of syntactic sugar to write.
  2) React: Does the diffing, optimizations, determining what the render and how.
  3) ReactDOM: Renders to the DOM. Other ways include React Native etc.
  4) Components in React are functions that returns a set of UI instructions that React uses to render HTML.
  5) Significantly easier to write JSX which looks like HTML.

React & ReactDOM part 2:
  1) React.createElement just replaces JSX.
  2) React.createElement has 3 variables to pass into.
    - String or component (class or functional)
    - Object (props/attributes).
    - Array (children).
  3) JSX is more readable, more pleasant developer experience.

ReactDOM v18 Changes:
  1) ReactDOM.render is being replaced with ReactDOM.createRoot

DOM Paint Flashing:
  1) Use Chrome DevTools -> More tools -> Rendering -> Paint flashing.
  2) Paint flashing determines what needs to be rendered.
  3) Repainting is when mount/modifies/unmount nodes.
  4) Repainting process is an expensive process (as mentioned before).
  5) Refresh repaints everything for the first time (mounting).
  6) Repainting whole page happens due to reflow (whole layout needs to be shifted).
  7) Reflow process is not that expensive.
