# Ex04 Simple Calculator - React Project
## Date: 28-03-2025

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
# app.js
```
import React, { useState } from "react";
import "./App.css";

const App = () => {
  const [input, setInput] = useState("");

  const handleClick = (value) => {
    if (value === "AC") {
      setInput(""); 
    } else if (value === "=") {
      try {
        setInput(eval(input).toString()); 
      } catch {
        setInput("Error");
      }
    } else {
      setInput(input + value); 
    }
  };

  return (
    <div className="calculator">
      <div className="display">{input || "0"}</div>
      <div className="buttons">
        <button className="btn-ac" onClick={() => handleClick("AC")}>AC</button>
        <button className="btn-special">⌫</button>
        <button className="btn-operator" onClick={() => handleClick("%")}>%</button>
        <button className="btn-operator" onClick={() => handleClick("/")}>/</button>

        <button className="btn-number" onClick={() => handleClick("7")}>7</button>
        <button className="btn-number" onClick={() => handleClick("8")}>8</button>
        <button className="btn-number" onClick={() => handleClick("9")}>9</button>
        <button className="btn-operator" onClick={() => handleClick("*")}>*</button>

        <button className="btn-number" onClick={() => handleClick("4")}>4</button>
        <button className="btn-number" onClick={() => handleClick("5")}>5</button>
        <button className="btn-number" onClick={() => handleClick("6")}>6</button>
        <button className="btn-operator" onClick={() => handleClick("-")}>-</button>

        <button className="btn-number" onClick={() => handleClick("1")}>1</button>
        <button className="btn-number" onClick={() => handleClick("2")}>2</button>
        <button className="btn-number" onClick={() => handleClick("3")}>3</button>
        <button className="btn-operator" onClick={() => handleClick("+")}>+</button>

        <button className="btn-number" onClick={() => handleClick("0")}>0</button>
        <button className="btn-number" onClick={() => handleClick(".")}>.</button>
        <button className="btn-equal" onClick={() => handleClick("=")}>=</button>
      </div>
      
      <footer>Designed by Harshini | Reg No: 212223220033</footer>

    </div>
  );
};

export default App;
```
# app.css
```
body {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  background-color: #290a97; 
  margin: 0;
}

.calculator {
  background: #605bc3;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.3);
  text-align: center;
}

.display {
  background: #2d2d2d;
  color: white;
  font-size: 2rem;
  text-align: right;
  padding: 15px;
  border-radius: 8px;
  margin-bottom: 10px;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

button {
  font-size: 1.5rem;
  font-weight: bold;
  padding: 15px;
  border: none;
  border-radius: 50%;
  cursor: pointer;
  transition: 0.3s ease;
  box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.2);
}

button:hover {
  opacity: 0.8;
}

button:active {
  transform: scale(0.95);
}

.btn-ac {
  background: #ff4d4d; 
  color: white;
}

.btn-equal {
  background: #ff9800; 
  color: white;
}

.btn-operator {
  background: #009688;
  color: white;
}

.btn-number {
  background: #4a148c; 
  color: white;
}

.btn-special {
  background: #4285f4; 
  color: white;
}

```


## OUTPUT
![image](https://github.com/user-attachments/assets/6518f35b-b906-4a75-b642-2e4d40aa4d5b)
![image](https://github.com/user-attachments/assets/ceb3f275-0177-457d-80a6-12307e56960f)



## RESULT
The program for developing a simple calculator in React.js is executed successfully.
