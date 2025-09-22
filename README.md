# MWAD-EXP_04-Simple-calculator
## Date:22/09/25
### Name: Rahul V
### Register No:212223040163

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

### Calculator.jsx
```
import React, { useState } from "react";
import "./Calculator.css";

function Calculator() {
  const [input, setInput] = useState("");
  const [result, setResult] = useState("");

  const handleClick = (value) => {
    setInput(input + value);
  };

  const handleClear = () => {
    setInput("");
    setResult("");
  };

  const handleEqual = () => {
    try {
      const evalResult = eval(input);
      setResult(evalResult);
    } catch {
      setResult("Error");
    }
  };

  return (
    <div className="calculator">
      <div className="display">{result || input || "0"}</div>
      <div className="buttons">
        <button onClick={handleClear} className="operator">C</button>
        <button onClick={() => handleClick("/")} className="operator">/</button>
        <button onClick={() => handleClick("*")} className="operator">*</button>
        <button onClick={() => handleClick("-")} className="operator">-</button>

        <button onClick={() => handleClick("7")}>7</button>
        <button onClick={() => handleClick("8")}>8</button>
        <button onClick={() => handleClick("9")}>9</button>
        <button onClick={() => handleClick("+")} className="operator">+</button>

        <button onClick={() => handleClick("4")}>4</button>
        <button onClick={() => handleClick("5")}>5</button>
        <button onClick={() => handleClick("6")}>6</button>
        <button onClick={handleEqual} className="equal">=</button>

        <button onClick={() => handleClick("1")}>1</button>
        <button onClick={() => handleClick("2")}>2</button>
        <button onClick={() => handleClick("3")}>3</button>
        <button onClick={() => handleClick("0")} className="zero">0</button>

        <button onClick={() => handleClick(".")}>.</button>
      </div>
    </div>
  );
}

export default Calculator;

```
### Calculator.css
```
body {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  background-color: #f5f5f5;
  margin: 0;
  font-family: 'Arial', sans-serif;
}

.calculator {
  width: 350px;
  padding: 20px;
  border-radius: 15px;
  background-color: #8c8b8b;
  border: 1px solid #ddd;
}

.display {
  font-size: 2rem;
  text-align: right;
  padding: 15px;
  margin-bottom: 15px;
  border-radius: 10px;
  background-color: #f0f0f0;
  color: #333333;
  min-height: 50px;
  word-wrap: break-word;
  border: 1px solid #ccc;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

button {
  padding: 20px;
  font-size: 1.2rem;
  border: none;
  border-radius: 10px;
  cursor: pointer;
  transition: background 0.2s ease;
  color: #333333;
  background-color: #e0e0e0;
}

button:hover {
  background-color: #d4d4d4;
}

.operator {
  background-color: #006eff;
  color: #fff;
}

.operator:hover {
  background-color: #0c30c3;
}

.equal {
  background-color: #4caf50;
  color: white;
  grid-row: span 2;
}

.equal:hover {
  background-color: #3e8e41;
}

.zero {
  grid-column: span 2;
}

@media (max-width: 500px) {
  .calculator {
    width: 90%;
  }
  button {
    padding: 15px;
    font-size: 1rem;
  }
  .display {
    font-size: 1.5rem;
  }
}

```
### App.jsx
```
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
<img width="1918" height="1089" alt="Screenshot 2025-09-22 143527" src="https://github.com/user-attachments/assets/e64925ee-a728-44b2-af82-53181df67dd3" />

<img width="1919" height="1100" alt="image" src="https://github.com/user-attachments/assets/61750487-1672-4ab5-8e9b-f1f73b8cc8ac" />

## RESULT
The program for developing a simple calculator in React.js is executed successfully.
