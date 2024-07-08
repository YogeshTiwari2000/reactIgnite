// type='module' : each JavaScript file is treated as a separate module
// Modules support the use of import and export statements for including functionality from other modules 
// Modules are in strict mode by default

//config driven UI means website acting different at different locations like diffent for delhi,and kolkata according to data supplied by backend api data
// rendering means updating something in dom/html
// ['functional components are normal functions at the end and props are there properties and parameters/args'] and ['state is another name for creating local variables'] and everything in react manages a state
//React ['Hooks are functions'] that allow functional components to use state which were previously only available in class components.(useState,useEffect,useContext,useReducer)
// we create var in react with useState and not like js_var(let a="hero") because react do not track js_var but '[with useState it manages virtual Dom and performs diff and reconsiliation]' algo but not with js_var
/// load page first then Api Data load and render ['useEffect() Hook']
//useEffect replaces lifecycle methods like componentDidMount, componentDidUpdate, and componentWillUnmount in class components.
<!-- const Title=()=>{
  return(
    <h1>Hello World</h1>
  ) 
}
<Title/>//same thing
{Title()}
 -->
// <React.Fragment></React.Fragment>it allows you to return multiple elements from a React component by allowing you to group a list of children without adding extra nodes to the DOM(shorthand version does not support the key attribute.)
Its like a empty tag

// npx is a tool that is used to execute the packages  It comes with npm then automatically npx will installed.
//  It is an npm package runner that can execute any package that you want from the npm registry without even installing that package.
// npx create-react-app is a command that allows you to use a package without installing it globally. It will download and execute the package on-the-fly, without permanently installing it on your machine.
// npm create-react-app is a command that installs the Create React App globally on your machine. Once installed, you can use it to create multiple React applications without needing to reinstall Create React App each time.

// DevDependencies should contain modules/packages a developer needs during development. such as, parcel, webpack, vite, mocha. These packages are necessary only while you are developing your project, not necessary on production.  
// Dependencies should contain library and framework in which your app is built on, needs to function effectively. such as Vue, React, Angular, Express, JQuery and etc. 
// These are the packages that the application needs for its normal operation and functionality when deployed.(in production environment)

                                   //#Tree shaking performed by webpacks
// Tree shaking is process of removing the unwanted code that we do not use while developing the application.

//                                     #pollyfills
// Polyfills help ensure cross-browser compatibility by converting our newer code to older versen of code
// we dont write pollyfills but bubble does/creates pollyfills automatically
// Feature Detection: Before applying a polyfill, developers often use feature detection to check whether a particular feature is supported by the user's browser. If the feature is missing or incomplete, the polyfill is loaded.
// Check if the 'fetch' API is supported
// if (!window.fetch) {
//   // If not, load the 'fetch' polyfill
//   import('whatwg-fetch').then(() => {
//     // Now you can safely use the 'fetch' API
//     fetch('https://api.example.com/data')
//       .then(response => response.json())
//   });

//                                           Virtual_Dom
//  Manipulating the Real DOM can be slow and resource-intensive, especially when dealing with frequent updates or changes.

// The ['Virtual DOM is a lightweight copy of the Real DOM']. It is a JavaScript representation of the DOM elements that React uses to keep track of changes.
// When a React ['component renders'], it creates a Virtual DOM representation of the UI elements.(tree like structure)

// [reconciliation] : When there is a chng in the state or props, React creates a new Virtual DOM representation of the updated UI.(['React-Fibre'] is new reconciliation engine for react-16 and it uses Dieff algo)
// The new Virtual DOM is then compared with the previous one through a process called "[reconciliation]."

//['Re-rendering Components'] : After identifying the differences, React update the Real DOM with the minimal set of changes required.
// Instead of updating the entire Real DOM, React only updates the specific parts that have changed.

//                                         JSX (JavaScript XML)
// with JSX Example : const myElement = <h1>I Love JSX!</h1>;
// without JSX Example const myElement = React.createElement('h1', {}, 'I do not use JSX!');
// common : const root = ReactDOM.createRoot(document.getElementById('root'));
// root.render(myElement);

// {TitleComponent} vs {<TitleComponent/>} vs {<TitleComponent></TitleComponent>} in JSX.
// {TitleComponent}: This value describes the TitleComponent as a javascript expression or a variable.
// <TitleComponent/> : In simple terms TitleComponent a function that is returning a JSX value. A component is written inside the {<  />} expression.
// <TitleComponent /> and <TitleComponent></TitleComponent> are equivalent ['only'] when < TitleComponent /> has no child components. The opening and closing tags are created to include the child components.
// <TitleComponent>
//     <FirstChildComponent />
//     <SecondChildComponent />
//     <ThirdChildComponent />
// </TitleComponent>

<!--  If the object accessed or function called is undefined or null , it returns undefined instead of throwing an error. Optional Chaining (?.) -->
