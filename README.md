# project-1
#html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="css.css">
    <title>Calculator</title>
</head>
<body>
    <div class="calculator">
        <div class="display">0</div>
        <button class="clear">C</button>
        <button class="operator">/</button>
        <button class="operator">+</button>
        <button class="operator">-</button>
        <button class="operator">*</button>
        <button class="operator">=</button>
        <button class="operator">1</button>
        <button class="operator">2</button>
        <button class="operator">3</button>
        <button class="operator">4</button>
        <button class="operator">5</button>
        <button class="operator">6</button>
        <button class="operator">7</button>
        <button class="operator">8</button>
        <button class="operator">9</button>
        <button class="operator">0</button>
        <button class="operator">.</button>

    </div>
   
    <script src="java.js"></script>
</body>
</html>



#css
/* Styles for the calculator container */
.calculator {
    width: 300px;
    margin: 0 auto;
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 10px;
    box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.2);
    background-color: #f5f5f5;
}

/* Styles for the display area */
.display {
    font-size: 24px;
    text-align: right;
    margin-bottom: 10px;
    padding: 10px;
    background-color: #fff;
    border: 1px solid #ccc;
    border-radius: 5px;
}

/* Styles for the calculator buttons */
button {
    font-size: 18px;
    padding: 10px 20px;
    margin: 5px;
    border: 1px solid #ccc;
    border-radius: 5px;
    background-color: #eee;
    cursor: pointer;
}

/* Style for the Clear button */
.clear {
    background-color: #ff6347; /* Red */
    color: #fff;
}

/* Style for the Equals button */
.equals {
    background-color: #008000; /* Green */
    color: #fff;
}

/* Style for the operator buttons */
.operator {
    background-color: #ffa500; /* Orange */
}

/* Style for the digit buttons */
.digit {
    background-color: #d3d3d3; /* Light Gray */
}



#js
function add(a, b) {
    return a + b;
}

function subtract(a, b) {
    return a - b;
}

function multiply(a, b) {
    return a * b;
}

function divide(a, b) {
    if (b === 0) {
        displayError("Cannot divide by zero");
        return;
    }
    return a / b;
}
function operate(operator, num1, num2) {
    switch (operator) {
        case '+':
            return add(num1, num2);
        case '-':
            return subtract(num1, num2);
        case '*':
            return multiply(num1, num2);
        case '/':
            return divide(num1, num2);
        default:
            return NaN; // Handle invalid operators
    }
}
const display = document.querySelector('.display');
const clearButton = document.querySelector('.clear');
const operatorButtons = document.querySelectorAll('.operator');
const digitButtons = document.querySelectorAll('.digit');
const equalsButton = document.querySelector('.equals');

// Add event listeners for buttons to handle user interactions
// You can use a variable to store the current input and operator.
const shekelsToDollarsButton = document.querySelector('.shekels-to-dollars');
const dollarsToShekelsButton = document.querySelector('.dollars-to-shekels');
const shekelsToEurosButton = document.querySelector('.shekels-to-euros');
const eurosToShekelsButton = document.querySelector('.euros-to-shekels');
const currencyInput = document.querySelector('.currency-input');
const currencyResult = document.querySelector('.currency-result');

// Add event listeners for currency conversion buttons
// Implement the conversion functions and update the result in the display.
