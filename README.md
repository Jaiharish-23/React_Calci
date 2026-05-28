# Ex04 Simple Calculator - React Project

## Name: JAI HARISH R

## Regno: 212224040124

## Date:26/05/26

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

### Calculator.js

```js
import React, { useState } from "react";
import "./Calculator.css";

function Calculator() {
  const [input, setInput] = useState("");

  const handleClick = (value) => {
    setInput(input + value);
  };

  const clearInput = () => {
    setInput("");
  };

  const backspace = () => {
    setInput(input.slice(0, -1));
  };

  const calculateResult = () => {
    try {
      setInput(eval(input).toString());
    } catch {
      setInput("Error");
    }
  };

  return (
    <div className="container">
      <div className="calculator">
        <h1>Calculator</h1>

        <input
          type="text"
          value={input}
          readOnly
          className="display"
        />

        <div className="buttons">
          <button className="gray" onClick={clearInput}>C</button>
          <button className="gray" onClick={backspace}>⌫</button>
          <button className="orange" onClick={() => handleClick("/")}>÷</button>
          <button className="orange" onClick={() => handleClick("*")}>×</button>

          <button onClick={() => handleClick("7")}>7</button>
          <button onClick={() => handleClick("8")}>8</button>
          <button onClick={() => handleClick("9")}>9</button>
          <button className="orange" onClick={() => handleClick("-")}>-</button>

          <button onClick={() => handleClick("4")}>4</button>
          <button onClick={() => handleClick("5")}>5</button>
          <button onClick={() => handleClick("6")}>6</button>
          <button className="orange" onClick={() => handleClick("+")}>+</button>

          <button onClick={() => handleClick("1")}>1</button>
          <button onClick={() => handleClick("2")}>2</button>
          <button onClick={() => handleClick("3")}>3</button>
          <button className="equal" onClick={calculateResult}>=</button>

          <button className="zero" onClick={() => handleClick("0")}>0</button>
          <button onClick={() => handleClick(".")}>.</button>
        </div>
      </div>
    </div>
  );
}

export default Calculator;
```

### Calculator.css

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
  background: linear-gradient(135deg, #141e30, #243b55);
  height: 100vh;
}

.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.calculator {
  width: 340px;
  padding: 25px;
  border-radius: 25px;
  background: #1f2937;
  box-shadow: 0 0 25px rgba(0, 0, 0, 0.5);
}

.calculator h1 {
  text-align: center;
  color: white;
  margin-bottom: 20px;
}

.display {
  width: 100%;
  height: 70px;
  border: none;
  border-radius: 15px;
  margin-bottom: 20px;
  padding: 15px;
  font-size: 32px;
  text-align: right;
  background: #111827;
  color: #00ffcc;
  outline: none;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 15px;
}

button {
  height: 65px;
  border: none;
  border-radius: 15px;
  font-size: 24px;
  cursor: pointer;
  background: #374151;
  color: white;
  transition: 0.2s;
}

button:hover {
  transform: scale(1.08);
  background: #4b5563;
}

.orange {
  background: #ff9500;
  color: white;
}

.orange:hover {
  background: #ffad33;
}

.equal {
  background: #00c896;
  color: white;
  grid-row: span 2;
  height: 145px;
}

.equal:hover {
  background: #00e6ac;
}

.gray {
  background: #6b7280;
}

.gray:hover {
  background: #9ca3af;
}

.zero {
  grid-column: span 2;
}
```

### App.js

```js
import React from "react";
import Calculator from "./Calculator";

function App() {
  return (
    <div>
      <Calculator />
    </div>
  );
}

export default App;
```

## OUTPUT


<img width="1914" height="1088" alt="image" src="https://github.com/user-attachments/assets/f0efbbe8-739d-41a0-9236-a86c157a7e09" />


<img width="1919" height="1080" alt="image" src="https://github.com/user-attachments/assets/fde755ed-942f-4575-889a-3e2abcbf633e" />


## RESULT
The program for developing a simple calculator in React.js is executed successfully.
