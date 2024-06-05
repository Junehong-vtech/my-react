# React
The library for web and native user interfaces.
- You can creates a Custom Tags with React.
- Components are like functions that return HTML elements. The simplest way to define a component is to write a JavaScript function.
- React Props are like function arguments in JavaScript and attributes in HTML. To send props into a component, use the same syntax as HTML attributes.
- React components has a built-in state object. The state object is where you store property values that belong to the component. When the state object changes, the component re-renders.
- React can perform actions based on user events. React has the same events as HTML: click, change, mouseover etc.
- event.preventDefault(): The preventDefault() method cancels the event if it is cancelable, meaning that the default action that belongs to the event will not occur.
- React onChange is an event handler that triggers when there is any change in the input field.
### Create React App
`$ mkdir react-app`  
`$ cd react-app`  
`react-app$ npx create-react-app .`  
### Edit React App
- `public/index.html` -> `src/index.js` -> `src/App.js`
- `src/index.css` and `src/App.css`

### React Hooks
Hooks allow function components to have access to state and other React features.  
Because of this, class components are generally no longer needed.
#### useEffect
The useEffect Hook allows you to perform side effects in your components.  
`useEffect` is a React Hook that lets you synchronize a component with an external system.  
Some examples of side effects are: fetching data, directly updating the DOM, and timers.  
`useEffect(setup, dependencies?)`  
###### Parameters
- `setup`: The function with your Effect’s logic. Your setup function may also optionally return a cleanup function. When your component is added to the DOM, React will run your setup function. After every re-render with changed dependencies, React will first run the cleanup function (if you provided it) with the old values, and then run your setup function with the new values. After your component is removed from the DOM, React will run your cleanup function.  
- optional `dependencies`: The list of all reactive values referenced inside of the setup code. Reactive values include props, state, and all the variables and functions declared directly inside your component body. If your linter is configured for React, it will verify that every reactive value is correctly specified as a dependency. The list of dependencies must have a constant number of items and be written inline like [dep1, dep2, dep3]. React will compare each dependency with its previous value using the Object.is comparison. If you omit this argument, your Effect will re-run after every re-render of the component.  
#### useState
The useState Hook allows us to track state in a function component.  
useState accepts an initial state and returns two values:  
  `The current state.`  
  `A function that updates the state.`  
  `// const _mode = useState('WELCOME');`  
  `// const mode = _mode[0];`  
  `// const setMode = _mode[1];`  
  `const [mode. setMode] = useState('WELCOME');`  
#### useMemo
The React `useMemo` Hook returns a memoized value. `Think of memoization as caching a value so that it does not need to be recalculated.`  
The `useMemo` Hook only runs when one of its dependencies update.  
This can improve performance.  

