# Getting started with React Bootstrap

![react bootstrap](https://res.cloudinary.com/uequations/image/upload/c_fit,e_sharpen:100,h_625,w_1200/v1637359162/Disruptive%20SmackTalk%20/getting-started-react-bootstrap/getting-started-react-bootstrap.jpg)
Author: <a href="https://www.linkedin.com/in/diaraye-sylla-398298161/" target="_blank" rel="noopener">Mensah Alkebu-Lan</a>

## Table of Contents
- [Install with Dependencies](#install-with-dependencies)
- [Let’s Develop](#lets-develop)
- [Let’s Run It](#lets-run-it)
- [References](#references)

## Install with Dependencies
If you’re using *npm init* to bootstrap your initial project, I would recommend using *src/index.js* when prompted for your *package.json* main as opposed to the default value *index.js*. If you’re prompted for a test command, use “react-scripts test.” We'll update the rest of the *package.json* later.  

Once the process is complete, you can use the following command to add the necessary dependencies to a newly created React Bootstrap-based project.

```bash
npm install react react-dom react-bootstrap react-scripts bootstrap@5.1.3
```

Notice, we’re using the 5.1.3 version of Bootstrap. Now, as hinted above, let’s create some folders in the root directory. Naturally, if you’re using *create-react-app*, some of these steps will already be done.

## Let’s Develop
First, create a public folder containing an *index.html* file.  A standard *index.html* file for a React application is the following:

```html
 <!DOCTYPE html>
<html lang="en">
 <head>
   <meta charset="utf-8" />
   <meta name="viewport" content="width=device-width, initial-scale=1" />
   <title>React-Bootstrap Starter</title>
 </head>
 <body>
   <noscript>You need to enable JavaScript to run this app.</noscript>
   <div id="root"></div>
 </body>
</html>
```

Then, create a *src* folder. To start, this can contain an empty *index.js*, *App.js*, and *App.css* file. 

Let's fill two of these files in. A standard *index.js* file for a React application is the following:

```js
import React from 'react';
import ReactDOM from 'react-dom';
import App from './App';
 
ReactDOM.render(<App />, document.getElementById('root'));
```

To use bootstrap, add the following import:
 
```js
import 'bootstrap/dist/css/bootstrap.min.css';
```

Notice the *index.js* file has an import that refers to App. Let’s add App to our App.js file.

```js
import React, { useState } from 'react';
import Container from 'react-bootstrap/Container';
import Button from 'react-bootstrap/Button';
 
import './App.css';
 
const App = () => (
   <Container>
       <Button variant="primary">Click Me!</Button>
   </Container>
);
 
export default App;
```

The *App.css* can be left blank and updated as needed.

## Let’s Run It
We’re almost ready to run this. We’re going to need to enact some changes in the *package.json* first. First let’s update “scripts” so we at least have the four basic commands:

```json
"scripts": {
   "test": "react-scripts test",
   "start": "react-scripts start",
   "build": "react-scripts build",
   "eject": "react-scripts eject"
 }
```

I know we don’t have unit tests. We’ll get to that next time.

What we have is quite simple, but it will run. When you try to run the app (i.e. *npm run start* or *yarn start*), you may be prompted to update *browserslist*. If not, just add it manually to your *package.json* file as is shown below.

```json
 "browserslist": {
   "production": [
     ">0.2%",
     "not dead",
     "not op_mini all"
   ],
   "development": [
     "last 1 chrome version",
     "last 1 firefox version",
     "last 1 safari version"
   ]
 }
```
 
Once start up is completed, you should be able to pull up your web app by pointing your browser to *http://localhost:3000*.

You can find the source code for this exercise on [Github](https://github.com/uequations/React-Bootstrap-Starter).
 
## References
1.  React-Bootstrap Documentation. https://react-bootstrap.github.io/getting-started/introduction/. Accessed 11/15/2021.
2.  Getting Started. https://react-bootstrap.github.io/getting-started/introduction/. Accessed 11/15/2021.
3.  How to Use React Bootstrap with NPM. https://www.pluralsight.com/guides/how-to-use-react-bootstrap-with-npm. Accessed 11/19/2021.
4.  react-bootstrap/react-bootstrap: Bootstrap components built with React. https://github.com/react-bootstrap/react-bootstrap. Accessed 11/19/2021.
