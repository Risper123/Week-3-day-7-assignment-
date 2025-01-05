Part 1: CSS3 Transitions and Animations
Task:

Use CSS transitions to create smooth effects on hover or focus (e.g., buttons that change color or grow).
Use CSS animations with @keyframes to create dynamic effects like fading, sliding, or rotating.
Requirements:

At least two elements must include hover or focus transitions.
At least two animations must be created using @keyframes (e.g., an animated banner or an animated loading spinner).
Part 2: JavaScript Functions
Task:

Write JavaScript functions to handle interactivity on the webpage.
Utilize parameters, return values, and demonstrate an understanding of scope.
Requirements:

Write at least three functions:
A function with parameters and return values (e.g., calculate a value like the area of a rectangle based on user input).
A function that demonstrates the concept of scope (local vs. global variables).
A function to toggle a CSS class that applies an animation (e.g., toggling a "hidden" class for a modal).
Part 3: Combining CSS Animations with JavaScript
Task:

Use JavaScript to trigger or control CSS animations dynamically.
Requirements:

Create an interactive element (e.g., a button, card, or slider) that triggers an animation when clicked.
Dynamically add or remove CSS classes to control the animation.
Ensure that the animation resets properly when triggered multiple times.


# Week-3-day-7-assignment-
My assignment for week 3 day 7

CSS Transitions Example:

/* Style for button with hover transition */
.button {
  background-color: #3498db;
  color: white;
  padding: 10px 20px;
  border: none;
  cursor: pointer;
  transition: background-color 0.3s ease-in-out, transform 0.3s ease-in-out;
}

.button:hover {
  background-color: #2980b9;
  transform: scale(1.1);
}

CSS Animation Example:

/* Animation for fading effect */
.fade-in {
  animation: fadeIn 2s ease-in-out;
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

/* Animation for sliding effect */
.slide-in {
  animation: slideIn 1s ease-in-out forwards;
}

@keyframes slideIn {
  from {
    transform: translateX(-100%);
  }
  to {
    transform: translateX(0);
  }
}

Function with Parameters and Return Values:

// Function to calculate area of a rectangle
function calculateArea(length, width) {
  return length * width;
}

// Example usage
let area = calculateArea(5, 10); // Returns 50
console.log("Area of rectangle:", area);


Function Demonstrating Scope:

let globalVariable = "I am global";

function demonstrateScope() {
  let localVariable = "I am local";
  console.log(globalVariable); // Access global variable
  console.log(localVariable);  // Access local variable
}

demonstrateScope();
// console.log(localVariable); // This would throw an error as localVariable is not accessible outside the function.


Function to Toggle CSS Classes:

function toggleAnimation(elementId, animationClass) {
  const element = document.getElementById(elementId);
  element.classList.toggle(animationClass);
}

Part 3: Combining CSS Animations with JavaScript

HTML Example:

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Animation Example</title>
  <style>
    .animated-box {
      width: 100px;
      height: 100px;
      background-color: #e74c3c;
      margin: 20px;
    }

    .bounce {
      animation: bounce 1s infinite;
    }

    @keyframes bounce {
      0%, 20%, 50%, 80%, 100% {
        transform: translateY(0);
      }
      40% {
        transform: translateY(-30px);
      }
      60% {
        transform: translateY(-15px);
      }
    }
  </style>
</head>
<body>

  <div id="box" class="animated-box"></div>
  <button onclick="toggleAnimation('box', 'bounce')">Bounce Box</button>

  <script>
    // Function to toggle animation
    function toggleAnimation(elementId, animationClass) {
      const element = document.getElementById(elementId);
      element.classList.toggle(animationClass);
    }
  </script>

</body>
</html>

