# Routing-tutorial
This a a practice code i wrote in learning to use Router. 


Installing a project requires more extension as in eslint.


npm init @eslint/config@latest

Note: npm init @eslint/config assumes you have a package.json file already. If you don’t, make sure to run npm init or yarn init beforehand.
After that, you can run ESLint on any file or directory like this:


npx eslint yourfile.js

What is Routing?

With Routing, we match different URL to different UI views(React components): routes 
Route refer to one of the matching that we did with React.
This enable users to navigate between different application screens, using the Browser URL.
It keeps UI in sync with the current Browser URL.
Routing only works in Client-side development. 

We define the routing routes in app to specify which component to display.
React Routing is handled by React router. 
https://reactrouter.com/

Note: Routing is important for SPA( Single page application) 


SPA( Single page application) 
Applications that is executed entirely on the client (Browser). 
React us used to update DOM. Routing eliminates need for reloading. 

Implementing Routing

Getting Started
There are three primary ways, or "modes", to use it in your app, so there are three guides to get you started.
Declarative
Data
Framework
Learn which mode is right for you 

In tutorial, we picked Declarative

import React from "react";
import ReactDOM from "react-dom/client";
import { BrowserRouter, Routes, Route } from "react-router";
//Defining root path

  <BrowserRouter>
    <Routes>
      <Route path="/" element={<App />} />
    </Routes>
  </BrowserRouter>

//Defining other paths



<Routes>
  <Route index element={<Home />} />
  <Route path="about" element={<About />} />

  <Route element={<AuthLayout />}>
    <Route path="login" element={<Login />} />
    <Route path="register" element={<Register />} />
  </Route>

  <Route path="concerts">
    <Route index element={<ConcertsHome />} />
    <Route path=":city" element={<City />} />
    <Route path="trending" element={<Trending />} />
  </Route>
</Routes>


 <a href="/pricing">Pricing</a>
This tag leads to another page but the it hard refreshes to link to a different page. React router does not use this. 

We can specify a Page Navigation component to that direct to all page in the SPA. Example below;

  <nav>
      <ul>
        <li>
          <Link to="/">Homepage</Link>
        </li>
        <li>
          <Link to="/pricing">Pricing</Link>
        </li>
        <li>
          <Link to="/product">Product</Link>
        </li>
      </ul>

Styling React with css

There are several option to styling react with css since the main purpose of react is to be unopinionated. 




Fundamental of CSS module

…
In using module for styling. You add “(global)” module to style selector to make make available in all instance. 

