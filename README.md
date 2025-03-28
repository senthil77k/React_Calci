# Ex04 Simple Calculator - React Project
## Date:28-03-2025

## AIM
To  develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM
### STEP 1
Create a React App.

### STEP 2
Open a terminal and run:
  <ul><li>npx create-react-app simple-calculator</li>
  <li>cd simple-calculator</li>
  <li>npm start</li></ul>

### STEP 3
Inside the src/ folder, create a new file Calculator.js and define the basic structure.

### STEP 4
Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

### STEP 5
Create a new file Calculator.css in src/ and add the styling.

### STEP 6
Open src/App.js and modify it.

### STEP 7
Start the development server.
  npm start

### STEP 8
Open http://localhost:3000/ in the browser.

### STEP 9
Test the calculator by entering numbers and operations.

### STEP 10
Fix styling issues and refine content placement.

### STEP 11
Deploy the website.

### STEP 12
Upload to GitHub Pages for free hosting.

## PROGRAM
#App.jsx
```
import React, { useState } from "react";
import "./App.css";
import FooterApp from "./footer";

function App() {
  const [input, setInput] = useState("");

  function handleClick(value) {
    setInput(input + value);
  }

  function clearInput() {
    setInput("");
  }

  function calculateResult() {
    try {
      setInput(eval(input).toString()); 
    } catch (error) {
      setInput("Error");
    }
  }

  return (
        <div className="calculator">
        <h2>Calculator</h2>
        <input type="text" value={input} readOnly />
        <div className="buttons">
          {["7", "8", "9", "/", "4", "5", "6", "*", "1", "2", "3", "-", "0", ".", "=", "+"].map(function (char) {
            return (
              <button key={char} onClick={char === "=" ? calculateResult : function () { handleClick(char); }}>
                {char}
              </button>
            );
          })}
          <button className="clear" onClick={clearInput}>Clear</button>
        </div>
        <div className="foot">
        <FooterApp ></FooterApp>
        </div>
      </div>

    
  );
}

export default App;
```
#footer.js
```
import React from "react";

const FooterApp = () => {
  return (
    <footer className="bg-gray-900 text-white py-6">
      <div className="container mx-auto text-center">
        {/* Navigation Links */}
        {/* Social Media Links */}

        {/* Copyright */}
        <p className="text-gray-400 text-sm">© {new Date().getFullYear()} Created by Senthil Kumaran 212223220103.</p>
      </div>
    </footer>
  );
};

export default FooterApp;
```
#App.css
```
body {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background: linear-gradient(to right, #ff7e5f, #feb47b, #86a8e7);
  font-family: Arial, sans-serif;
}

.calculator {
  background: linear-gradient(135deg, #ff7e5f, #feb47b);
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
  text-align: center;
  width: 250px;
}

h2 {
  margin-bottom: 10px;
}

input {
  width: 100%;
  height: 40px;
  text-align: right;
  font-size: 1.5em;
  padding: 5px;
  margin-bottom: 10px;
  border: 1px solid #e6d7d7;
  border-radius: 5px;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 5px;
}

button {
  padding: 10px;
  font-size: 1.2em;
  background: #3498db;
  color: rgb(255, 255, 255);
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

button:hover {
  background: #2980b9;
}

.clear {
  grid-column: span 4;
  background: #e74c3c;
}

.clear:hover {
  background: #c0392b;
}

.foot{
  
  padding: 20px 0;
  border-radius: 10px;
  position: fixed;
  bottom: 0;
  left: 38%;
  text-align: center;
}
```
#index.html
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>React App</title>
</head>
<body>
  <div id="root"></div>
</body>
</html>
```
## OUTPUT
![WhatsApp Image 2025-03-28 at 22 04 08_1b6f6e7b](https://github.com/user-attachments/assets/5f062141-2f26-4e08-8b87-4850c365a592)

![WhatsApp Image 2025-03-28 at 22 04 20_2833ba91](https://github.com/user-attachments/assets/17782671-e551-4626-8bc5-001d2a02e3dc)

![WhatsApp Image 2025-03-28 at 22 04 29_0f61cbc2](https://github.com/user-attachments/assets/c16d7a64-c238-4f65-bc96-b54f6acef710)

## RESULT
The program for developing a simple calculator in React.js is executed successfully.
