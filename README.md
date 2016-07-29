# React Intro Workshop / Demo

React is the new hotness on the Javascript block. This demo / workshop will take you from zero to hero in a matter of github branches.

### How To Use This Repo

I've separated each learning objective into its own github branch. We'll start with the basics and gradually build up to a fully fledged React app.

To get started, simply clone this repo and open the files in your favorite text editor.

### 1. The Super Basics

React is a library like jQuery or Angular that helps us interact with the DOM. It was created by Facebook for two main reasons: modularity and performance.

A platform like Facebook has a ton of moving parts. Trying to keep track of them all in a single codebase gets pretty unwieldy after a certain number of lines of code. React is built on components - small, (mostly) independent pieces of code that can be added, removed and modified as needed without worrying too much about the overall codebase.

Facebook also has a ton of users, which means performance is key. DOM manipulation is expensive, meaning that the more times you have to change the DOM, the slower your application will run. React utilizes a "virtual DOM" - I picture it like a hash map of the actual DOM - and lifecycle hooks to optimize the when, where and how of DOM manipulation.

With performance and modularity in mind, let's dive into the HTML index file.

### The React Library

For now, I'll use script tags and bower to manage my dependencies. Later we'll pull in npm and webpack as our preferred packaging managers.

To get started with React, we need the react.js library as well as react-dom.js, the virtual DOM library.

Since many features depend on the latest javascript language features (ES2015) as well as React's convenient html tag shorthand JSX, we'll use babel as our transpiler via CDN.

### Hello World

Go ahead now and bower install those dependencies and start up a simple python HTTP server.

To test if it's working, open up chrome to your local host server. You should see a little welcome message from React.

Inside our HTML body, we have a div id="root". The script tag below it (note the "text/babel" type) executes a call to ReactDOM's render method. We're telling it to render the h1 element to the previously-defined root element. The h1 there is JSX - a shorthand for ReactDOM method calls.

We don't need JSX by the way. Open up the dev tools in chrome and try this command:

    ReactDOM.render(
      React.createElement('p', null, 'Hello World'), document.getElementById('root');
    )

As you can see, JSX is simply making it a little easier for us to use React to create new HTML elements for rendering by ReactDOM.

That's it for our intro, head to the "first_component" branch for the next step.
