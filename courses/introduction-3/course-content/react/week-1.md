# 1 - React 101

### What is NPM?

When you installed Node, you also installed a package managing application called [`npm`](https://www.npmjs.com/). `npm` will install JavaScript packages in your project and also keep track of details about the project.

The [Node.js Package Manager (npm)](https://www.npmjs.com/) is the default and most popular package manager in the Node.js ecosystem, and is primarily used to install and manage external modules in a Node.js project. It is also commonly used to install a wide range of CLI tools and run project scripts. npm tracks the modules installed in a project with the `package.json` file, which resides in a project’s directory and contains:

* All the modules needed for a project and their installed versions
* All the metadata for a project, such as the author, the license, etc.
* Scripts that can be run to automate tasks within the project

As you create more complex Node.js projects, managing your metadata and dependencies with the `package.json` file will provide you with more predictable builds, since all external dependencies are kept the same. The file will keep track of this information automatically; while you may change the file directly to update your project’s metadata, you will seldom need to interact with it directly to manage modules.

### What is create-react-app?

Starting a new React project used to be a complicated multi-step process that involved setting up a build system, a code transpiler to convert modern syntax to code that is readable by all browsers, and a base directory structure. But now, [Create React App](https://github.com/facebook/create-react-app) includes all the JavaScript packages you need to run a React project, including code transpiling, basic linting, testing, and build systems. It also includes a server with _hot reloading_ that will refresh your page as you make code changes. Finally, it will create a structure for your directories and components so you can jump in and start coding in just a few minutes.

`npm` also includes a tool called [`npx`](https://www.npmjs.com/package/npx), which will run executable packages. What that means is you will run the Create React App code without first downloading the project.

The executable package will run the installation of `create-react-app` into the directory that you specify. It will start by making a new project in a directory, which in this tutorial will be called `pokedex`. Again, this directory does not need to exist beforehand; the executable package will create it for you. The script will also run `npm install` inside the project directory, which will download any additional dependencies.

To install the base project, run the following command:

```
npx create-react-app pokedex
```

This command will kick off a build process that will download the base code along with a number of dependencies.

Now your project is set up in a new directory. Change into the new directory:

```
cd pokedex
```

Now that you are inside the project directory, take a look around. You can either open the whole directory in your text editor, or if you are on the terminal you can list the files out with the following command:

```
ls -a
```

&#x20;The `-a` flag ensures that the output also includes hidden files.

Either way, you will see a structure like this:

```
Output
node_modules/
public/
src/
.gitignore
README.md
package-lock.json
package.json
```

Let’s explain these one by one:

* `node_modules/` contains all of the external JavaScript libraries used by the application. You will rarely need to open it.
* The `public/` directory contains some base HTML, JSON, and image files. These are the roots of your project.
* The `src/` directory contains the React JavaScript code for your project. Most of the work you do will be in that directory. You can delete all the files inside this directory and create the files as you need them.
* The `.gitignore` file contains some default directories and files that git—your source control—will ignore, such as the `node_modules` directory. The ignored items tend to be larger directories or log files that you would not need in source control. It also will include some directories that you’ll create with some of the React scripts.
* `README.md` is a markdown file that contains a lot of useful information about Create React App, such as a summary of commands and links to advanced configuration. For now, it’s best to leave the `README.md` file as you see it. As your project progresses, you will replace the default information with more detailed information about your project.

The last two files are used by your package manager. When you ran the initial `npx` command, you created the base project, but you also installed the additional dependencies. When you installed the dependencies, you created a `package-lock.json` file. This file is used by `npm` to ensure that the packages match exact versions. This way if someone else installs your project, you can ensure they have identical dependencies. Since this file is created automatically, you will rarely edit this file directly.

The last file is a `package.json`. This contains metadata about your project, such as the title, version number, and dependencies. It also contains scripts that you can use to run your project.

Start the project by typing the following command in the root of your project. For this tutorial, the root of your project is the `pokedex` directory. Be sure to open this in a separate terminal or tab, because this script will continue running as long as you allow it:

```
npm start
```

&#x20;You’ll see some placeholder text for a brief moment before the server starts up, giving this output:

```
Compiled successfully!

You can now view digital-ocean-tutorial in the browser.

  http://localhost:3000

Note that the development build is not optimized.
To create a production build, use npm run build.
```

If you are running the script locally, it will open the project in your browser window and shift the focus from the terminal to the browser.

If that doesn’t happen, you can visit [`http://localhost:3000/`](http://localhost:3000/) to see the site in action. If you already happen to have another server running on port `3000`, that’s fine. Create React App will detect the next available port and run the server with that. In other words, if you already have one project running on port `3000`, this new project will start on port `3001`.

### What is React?

React is a JavaScript library created by Facebook. It is used for making complex, interactive user interfaces. It has become very popular in the last 5 years.

Why has it become so popular?

* It is fast and efficient
* It is easy to understand & less verbose than the "vanilla" JS API
* It helps separate functionality into small, understandable pieces

### What is a component? <a href="#what-is-a-component" id="what-is-a-component"></a>

React heavily relies on a concept called "components". Components are like small Lego blocks for designing and developing user interfaces (UI). They can be stuck together in different ways to create new UI.

Let's have a look at an example: the GitHub header. What are the logical "pieces" of UI? What could be a component?

![](<../../../../.gitbook/assets/image (203).png>)

Here we've highlighted some elements that could be components:

![](<../../../../.gitbook/assets/image (89).png>)

#### Component tips <a href="#component-tips" id="component-tips"></a>

There are no hard & fast rules for making components. UIs can be split up into components in many different ways, requiring judgement based on your context.

* Components should follow the Single Responsibility Principle
  * Each component should only have 1 "responsibility"
  * Should only do 1 thing
* Components should have good, explicit names
  * This helps you to remember what the component's job is

| Exercise A (estimate: 10 min)                                                                                                                                     |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1. Look at the example online shopping user interface in the [Thinking in React article](https://reactjs.org/docs/thinking-in-react.html) (the image at the top). |
| 2. Draw boxes around the components and give them names. Compare with the example components shown in the second image.                                           |

### Rendering with React <a href="#rendering-with-react" id="rendering-with-react"></a>

Remember how annoying it was to manage the DOM yourself in [our previous lesson](https://github.com/Migracode-Barcelona/javascript-module-2-todo-workshop#create-and-manipulate-dom-elements)? The "vanilla" JavaScript APIs for updating the DOM are quite long and difficult to remember. React makes this easier by manipulating each DOM element itself, instead of you doing it manually. You give React a "description" of the DOM that you want and it will update the DOM for you. React _abstracts_ away the management of the DOM.

Let's take a look at an example. We are going to walk through how to render a `<div>` with the text "Hello World" within it.

First, lets recap how we could do this using "vanilla" JS ([interactive version](https://jsbin.com/zexiyulavu/edit?html,output)):

```
let divNode = document.createElement("div");
divNode.innerText = "Hello World";

let rootElement = document.querySelector("#root");
rootElement.appendChild(divNode);
```

Now let's convert to using React ([interactive version](https://jsbin.com/calaqitede/1/edit?html,output)):

```
const element = React.createElement("div", {
  children: "Hello World",
});

const rootElement = document.querySelector("#root");
ReactDOM.render(element, rootElement);
```

### JSX <a href="#jsx" id="jsx"></a>

As you can see, React is already helping us a bit by cleaning up some of the verbose vanilla JS APIs. However in a typical React application you would still use a _lot_ of the `React.createElement` function. To improve the developer experience the React team developed **JSX**.

JSX is a simple syntax _sugar_ that looks like HTML, but is actually converted to the `React.createElement` function when you run it.

Using JSX ([interactive version](https://jsbin.com/gabujocuda/edit?html,output)):

```
const element = <div>Hello World</div>;

const rootElement = document.querySelector("#root");
ReactDOM.render(element, rootElement);
```

As you can see, this is much easier to read than both the straight `React.createElement` API and the vanilla JS API. Most people using React use JSX to write their components.

| Exercise B (estimate: 5 min)                                                                                                                           |
| ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Change the [JSX example from above](http://jsbin.com/gekahexige/edit?html,output) to instead render a `h1` tag with the text "Hello Code Your Future". |

### Let's create a React app <a href="#lets-create-a-react-app" id="lets-create-a-react-app"></a>

| Exercise C (estimate: 10 min)                                                                    |
| ------------------------------------------------------------------------------------------------ |
| 1. If you haven't already, follow the instructions above to create a React app called `pokedex`. |

#### What got created? <a href="#what-got-created" id="what-got-created"></a>

Diagram of folder layout created by create-react-app. Click [here](https://excalidraw.com/#json=5666421027635200,SRigco8\_OhrCb94QSj4Wow) for live diagram.

![](<../../../../.gitbook/assets/image (127).png>)

### React Components <a href="#react-components" id="react-components"></a>

We looked at the beginning of the lesson at the concept of components. Now let's look at how components are made in React.

```
import React from "react";
import ReactDOM from "react-dom";

function HelloWorld() {
  return <div>Hello World</div>;
}

ReactDOM.render(<HelloWorld />, document.querySelector("#root"));
```

There are 3 important parts in this code:

1. First we import `React`. This is important because&#x20;
   1. The code we write in a React app is written in JSX. JSX is an extension of the JavaScript language based on ES6, which allows us to write HTML elements in JavaScript and place them in the DOM without any `createElement()`  and/or `appendChild()` methods.
   2. &#x20;Behind the scene JSX is translated to JavaScript and it is when we need `React.createElement` and If we don't import "react" then `React` variable will be undefined and our React app will fail to run.
2. We create a React component called `HelloWorld`.
3. We _render_ the `HelloWorld` component into the element with the id of `root`. This element with id of `root` is inside `index.html` file inside _public_ directory.

**Note :- The process of **_**rendering**_** is converting the JSX elements returned by the component function into DOM elements on the screen. This is done by React for you.**

| Exercise D (estimate: 10 min)                                                                                                                                                                                                             |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1. In the `pokedex` React app that you just created, open the `src/App.js` file.                                                                                                                                                          |
| 2. Delete everything in the file except the line containing `export default App`. You should see an error in your terminal and in your web browser - don't panic! We're going to remake the `App` component ourselves.                    |
| 3. Import the React variable from the React package.                                                                                                                                                                                      |
| 4. Create a function named `App`, which will be our component.                                                                                                                                                                            |
| 5. Within the `App` function, return a `<h1>` element with the text "Welcome to the Pokedex". What do you see in your web browser?                                                                                                        |
| 6. Create a `<div>` element that _wraps around_ the `<h1>` you just created.                                                                                                                                                              |
| 7. Below the `<h1>` element (but within the `<div>`), create an `<img>` element. Then make its `src` attribute equal to `https://assets.pokemon.com/assets/cms2/img/pokedex/full/016.png`. What do you expect to see in your web browser? |
| 8. Now create a `<header>` element to wrap both the `<h1>` element **and** the `<img>` element.                                                                                                                                           |

**Component Composition**

A component can be combined with another component so that both are rendered. This is called _composition_ ([interactive example](https://codesandbox.io/s/0x4wonqn00)):

```
function Greeting() {
  return <span>Hello</span>;
}

function Mentor() {
  return <span>Ali</span>;
}

function HelloWorld() {
  return (
    <div>
      <Greeting />
      <Mentor />
    </div>
  );
}
```

In the `HelloWorld` component we are using a reference to the `Greeting` and `Mentor` components. React reads these references when rendering `HelloWorld` and so it renders the `Greeting` and `Mentor` _child_ components.

We are also using some shorter syntax within the `HelloWorld` component. `<Greeting />` is just a shorter way of writing `<Greeting></Greeting>`, which is useful if we don't need to put anything inside the `Greeting` component.

Notice how the components that we write (`HelloWorld`, `Greeting`, `Mentor`) are written using a `camel case` convention and always start with an uppercase letter? And "regular DOM" components (`div`, `span`) are always lowercase? This is a convention to let you know whether you are using a "regular DOM component" or a component that you have written. When you're making your own components, you should always start them with an uppercase letter.

| Exercise E (estimate: 5 min)                                                                                                                                                     |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1. In your `pokedex` React app, open the `src/App.js` file.                                                                                                                      |
| 2. Create a new function named `Logo`.                                                                                                                                           |
| 3. Copy the `<header>` element and its contents and paste it into the `Logo` component.                                                                                          |
| 4. Replace the `<header>` element in the `App` component with the new `Logo` component.                                                                                          |
| 5. Create a new component function named `BestPokemon` and return a `<p>` element with some text saying which is your favorite Pokémon (e.g. "My favorite Pokémon is Squirtle"). |
| 6. _Render_ your new `BestPokemon` component below the `Logo` component within the `App` component.                                                                              |

**Arrow Functions for shorter syntax**

Because a React component is just a function, we can also use the arrow function syntax:

```
const HelloWorld = () => {
  return (
    <div>
      <h1>Hello World</h1>
    </div>
  );
};
```

This can be even shorter again if we use parentheses and implicit return:

```
const HelloWorld = () => (
  <div>
    <h1>Hello World</h1>
  </div>
);
```

Although this is shorter, it is less flexible as we cannot insert code that is **not** JSX. Like for example, a `console.log`:

```
// THIS DOES NOT WORK!
const HelloWorld = () => (
  console.log('Hello!');
  <div>
    <h1>Hello World</h1>
  </div>
);
```

If we want to do this, we can still use arrow functions but we can't use the implicit return.

| Exercise F (estimate: 5 min)                                                           |
| -------------------------------------------------------------------------------------- |
| 1. Using the `pokedex` React app that you created earlier, open the `src/App.js` file. |
| 2. Convert the `Logo` and `BestPokemon` functions into arrow functions.                |

### Embedding JavaScript into JSX <a href="#embedding-javascript-into-jsx" id="embedding-javascript-into-jsx"></a>

So far all of the components we have looked at haven't been able to change - they are _hard-coded_. But this doesn't make very interesting websites, we want to be able to use variables with different data. We can insert variables (and some other things) into our React components.

Anything in the JSX that is inside curly braces `{}` is interpreted as a regular JavaScript _expression_. That means you can use every object or function from JavaScript that we have learned so far. Let's look at an example ([interactive example](https://codesandbox.io/s/interpolation-in-jsx-l910pqnjql)):

```
function Greeting() {
  const greetingWord = "Hello";

  return <span>{greetingWord}</span>;
}
```

Now instead of hard-coding the greeting in the `Greeting` component, we are using a variable. Remember that everything between the curly braces is just regular JavaScript. So we can use more than just variables ([interactive example](https://codesandbox.io/s/interpolation-with-methods-in-jsx-nw29kzx744?file=/src/HelloWorld.js)):

```
function Mentor() {
  const mentors = ["Ali", "Kash", "Davide", "German", "Gerald"];
  return <span>{mentors.join(", ")}</span>;
}
```

Now we have modified the `Mentor` component to use the `Array.join` method so that it lists several mentor's names. This also works with other JS types:

```
function Addition() {
  return <span>{1 + 2 + 3}</span>;
}
```

```
function Weather() {
  const weatherData = {
    temperature: 5,
    location: "London",
  };

  return (
    <p>
      The temperature in {weatherData.location} is {weatherData.temperature}
    </p>
  );
}
```

```
function formatName(user) {
  return user.firstName + " " + user.lastName;
}

function Name() {
  const user = {
    firstName: "Bob",
    lastName: "Marley",
  };
  return <span>{formatName(user)}</span>;
}
```

A common pattern in React is to use `Array.map` to loop through a list of items and render a component for each one ([interactive example](https://codesandbox.io/s/interpolation-with-map-in-jsx-7mw0mw3qx0?file=/src/MentorsList.js)):

```
const mentors = ["Ali", "Kash", "Davide", "German", "Gerald"];

function MentorsList() {
  return (
    <ul>
      {mentors.map((name) => (
        <li>{name}</li>
      ))}
    </ul>
  );
}
```

Here we are using `Array.map` to turn an array of strings into an array of components.

| Exercise G (estimate: 10 min)                                                                                                                                                                                           |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1. Using the `pokedex` React app that you created earlier, open the `src/App.js` file.                                                                                                                                  |
| 2. Inside the `Logo` component create a new variable called `appName` and assign it to `"Pokedex"`.                                                                                                                     |
| 3. Now replace the hard-coded app name with `{appName}`. What do you see in your web browser? What would you do if you wanted to change the app name?                                                                   |
| 4. Create a new component named `CaughtPokemon`. Within this component return a `<p>` tag with the text "Caught 0 Pokémon on" (we're going to fill in today's date in the next step).                                   |
| 5. Create a variable named `date` within the `CaughtPokemon` component, and assign it today's date (hint: `new Date().toLocaleDateString()`). Finally, render the `date` variable after the text "Caught 0 Pokémon on". |
| 6. Render the `CaughtPokemon` component within the `App` component (below `BestPokemon`).                                                                                                                               |
| 7. Within the `BestPokemon` component, create a variable named `abilities` and assign it to an array with some Pokémon abilities (e.g. `['Anticipation', 'Adaptability', 'Run-Away']`).                                 |
| 8. Change the `BestPokemon` component to return a `<div>` element with the existing `<p>` element inside it. Then add a `<ul>` element underneath the `<p>` element.                                                    |
| 9. Now use the `.map()` method on the `abilities` variable to loop over each name and return a `<li>` element for each (hint: look at the mentors list example above) within the `<ul>` element.                        |

### Keys <a href="#keys" id="keys"></a>

You may have noticed that we are now seeing a red error message in the Dev Tools: `Warning: Each child in a list should have a unique "key" prop.`. This error happens when you use `Array.map` to return a list of elements ([interactive example](https://codesandbox.io/s/key-prop-for-lists-in-react-pwp8ox4kn0?file=/src/MentorsList.js)):

```
const mentors = ["Ali", "Sub", "Loic", "Anthony", "Lucy", "Mozart"];

function MentorsList() {
  return (
    <ul>
      {mentors.map((name, index) => (
        <li key={index}>{name}</li>
      ))}
    </ul>
  );
}
```

Here we have added a `key` prop to the `li` element. A documentation page explaining in more depth is in the further reading section but basically the `key` prop has a special meaning in React because it is used internally to keep track of which element in the list is which.

### Importing/Exporting Components <a href="#importingexporting-components" id="importingexporting-components"></a>

To help organize your code, components can be imported and exported just like any other JavaScript code ([interactive example](https://codesandbox.io/s/1z6xozl81l)):

```
import Greeting from "./Greeting";
import Mentor from "./Mentor";

function HelloMentor() {
  return (
    <div>
      <Greeting />
      <Mentor />
    </div>
  );
}
```

We also need to export our components if we want to use them in other files:

```
function Greeting() {
  return <span>Hello</span>;
}

export default Greeting;
```

The convention is to name component files exactly the same as the component (including the capital letter).

| Exercise H (estimate: 5 min)                                                                                                |
| --------------------------------------------------------------------------------------------------------------------------- |
| 1. Open the `pokedex` React app that you created earlier.                                                                   |
| 2. Create a new file within the `src` directory named `Logo.js`.                                                            |
| 3. Copy and paste the `Logo` component from `App.js` into `Logo.js`.                                                        |
| 4. Remember to add `import React from 'react'` at the top of `Logo.js`.                                                     |
| 5. Export the `Logo` component from `Logo.js` (hint: look at the `Greeting` example above).                                 |
| 6. Delete the old `Logo` component from `App.js`.                                                                           |
| 7. Import the `Logo` component into `App.js` (hint: look at the `HelloMentor` example above).                               |
| 8. Repeat this process with the `BestPokemon` and `CaughtPokemon` components. What do you think the files should be called? |

### Making an argument for Props <a href="#making-an-argument-for-props" id="making-an-argument-for-props"></a>

What's the problem with our `HelloMentor` component above?

The component `HelloMentor` is very static. What if we want to say _hello_ to a different mentor? Currently, we would have to change the code too! This is easy in our tiny application but for "real" applications this might be more difficult.

Instead wouldn't it be good if we could change which mentor we are saying hello to every time we render the component? So we could reuse the `HelloMentor` component for different mentor names. This is what _props_ are for.

### What are Props? <a href="#what-are-props" id="what-are-props"></a>

Props are what we use in React to pass "arguments" to components. They are very similar to arguments in functions - you can "pass" props to components, and you can use those props within a component.

First let's look at passing props to your components ([interactive example](https://codesandbox.io/s/intro-to-props-vmjy0o91m7?file=/src/HelloMentor.js)):

```
<Mentor name="Mozafar" />
```

As you can see props are key-value pairs, in this example the key is `name` and the value is the string `'Mozafar'`. We can pass as many props as we like to a component.

We don't have to use strings, we can use any valid JavaScript data like numbers, arrays and objects. Remember that in JSX you can use curly braces `{}` to inject data that is not a string:

```
<Mentor age={30}>
```

Now let's take a look at using props that we have passed to a component ([interactive example](https://codesandbox.io/s/intro-to-props-vmjy0o91m7?file=/src/Mentor.js)):

```
function Mentor(props) {
  console.log(props);
  return <span>{props.name}</span>;
}
```

React gives you access to props in the **first argument** to the component function. We can then inject props into our component using curly braces.

The `props` variable is just a normal object with key-value pairs that match what was passed to the component. Because it is just a variable, it can be used like any other variable. That includes injecting props into attributes:

```
<div id={"mentor-id-" + props.id}>{props.name}</div>
```

Or calculating new values:

```
<div>{props.age + 1}</div>
```

| Exercise I (estimate: 10 min)                                                                                                                                                 |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1. Using the `pokedex` React app that you created earlier, open the `App.js` file.                                                                                            |
| 2. Pass a prop `appName="Pokedex"` to the `Logo` component.                                                                                                                   |
| 3. Now open the `Logo.js` file.                                                                                                                                               |
| 4. Delete the `appName` variable. What do you see in your web browser? Why?                                                                                                   |
| 5. Change the `Logo` function to access the first argument and call it `props`. Use `console.log` to inspect the `props` variable.                                            |
| 6. Change the usage of `appName` in the `<h1>` to be `props.appName` instead. Does this fix the problem? Why?                                                                 |
| 7. Now open the `BestPokemon.js` file.                                                                                                                                        |
| 8. Copy the `abilities` variable and then delete it from `BestPokemon.js`.                                                                                                    |
| 9. Paste the `abilities` variable into `App.js`.                                                                                                                              |
| 10. Pass the `abilities` variable as a prop to `BestPokemon` from `App.js`.                                                                                                   |
| 11. In the `BestPokemon.js` file replace the existing usage of `abilities` with the `abilities` **prop**. You should still see the Pokémon ability names in your web browser. |
| 12. **(STRETCH GOAL)** Repeat the process with the `date` variable in the `CaughtPokemon.js` file.                                                                            |

