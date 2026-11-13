# EXP 12 – Simple Single Page Application (SPA) Using React

**NAME:** Nithya T  
**REG NO:** 2305001023

## Aim

To develop a simple Single Page Application (SPA) using React JS with Home, About, and Contact pages and navigate between them using the useState hook.

## Objectives

- To understand the concept of Single Page Applications.
- To create reusable components in React.
- To use the useState hook for managing state.
- To implement navigation between different pages without reloading the browser.
- To apply CSS styling to the React application.

## Program

### Step 1: Create a React Project

```bash
npm create vite@latest react-spa
cd react-spa
npm install
npm run dev
```

Select React as the framework and JavaScript as the variant.

### Step 2: App.jsx

```jsx
import { useState } from "react";
import "./App.css";

function Home() {
  return (
    <div>
      <h2>Home Page</h2>
      <p>Welcome to Nithya's React SPA!</p>
    </div>
  );
}

function About() {
  return (
    <div>
      <h2>About Page</h2>
      <p>This is a simple Single Page Application.</p>
    </div>
  );
}

function Contact() {
  return (
    <div>
      <h2>Contact Page</h2>
    </div>
  );
}

function App() {
  const [page, setPage] = useState("home");

  return (
    <div className="app">
      <h1>Simple React SPA</h1>

      <nav>
        <button onClick={() => setPage("home")}>Home</button>
        <button onClick={() => setPage("about")}>About</button>
        <button onClick={() => setPage("contact")}>Contact</button>
      </nav>

      <hr />

      {page === "home" && <Home />}
      {page === "about" && <About />}
      {page === "contact" && <Contact />}
    </div>
  );
}

export default App;
```

### Step 3: App.css

```css
.app {
  text-align: center;
  padding: 30px;
}

nav {
  margin: 20px;
}

button {
  margin: 5px;
  padding: 10px 20px;
  cursor: pointer;
  background-color: blue;
  color: white;
  border: none;
  border-radius: 5px;
}

button:hover {
  background-color: darkblue;
}
```

### Step 4: index.css

```css
body {
  font-family: Arial, sans-serif;
  text-align: center;
  background-color: #f2f2f2;
}

h1 {
  color: darkblue;
}

h2 {
  color: darkgreen;
}
```

### Step 5: main.jsx

```jsx
import React from "react";
import ReactDOM from "react-dom/client";
import App from "./App.jsx";
import "./index.css";

ReactDOM.createRoot(document.getElementById("root")).render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);
```

## Output

### 1. Home Page



<img width="1185" height="677" alt="image" src="https://github.com/user-attachments/assets/46e0f9c6-ce51-4e6f-b150-197a26f83489" />


### 2. About Page

<img width="437" height="336" alt="image" src="https://github.com/user-attachments/assets/d053f215-3a0b-4e5e-95cb-507e4f53b525" />

### 3. Contact Page


<img width="1072" height="682" alt="image" src="https://github.com/user-attachments/assets/086a6bd0-2793-4ba9-9412-6f3e88e5262f" />


## Result

Thus, a simple Single Page Application was successfully developed using React JS with Home, About, and Contact pages. Navigation between the pages was implemented using the useState hook without reloading the browser.
