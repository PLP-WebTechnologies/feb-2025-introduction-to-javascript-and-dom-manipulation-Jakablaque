# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.


# Tasks
- Create a well-structured HTML5 document.
-- Ensur Use at least 5 different HTML elements.
e semantic correctness.

Happy Coding! 💻✨


<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>JavaScript DOM Demo</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <header>
    <h1 id="main-title">Welcome to My Official Page</h1>
  </header>

  <section>
    <article>
      <p id="text">This is a dynamic paragraph.</p>
      <button onclick="changeText()">Change Text</button>
      <button onclick="changeStyle()">Change Style</button>
      <button onclick="addElement()">Add Element</button>
      <button onclick="removeElement()">Remove Element</button>
    </article>
  </section>

  <div id="container"></div>

  <footer>
    <p>&copy; 2025 Demo Page</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>



file.js


function changeText() {
  const paragraph = document.getElementById('text');
  paragraph.textContent = 'The text has been updated!';
}

function changeStyle() {
  const paragraph = document.getElementById('text');
  paragraph.style.color = 'blue';
  paragraph.style.fontSize = '20px';
  paragraph.style.backgroundColor = '#f0f0f0';
}

function addElement() {
  const container = document.getElementById('container');
  const newElement = document.createElement('p');
  newElement.textContent = 'This is a new paragraph added dynamically!';
  newElement.id = 'dynamic-paragraph';
  container.appendChild(newElement);
}

function removeElement() {
  const existing = document.getElementById('dynamic-paragraph');
  if (existing) {
    existing.remove();
  } else {
    alert("No element to remove!");
  }
}

index.css

body {
  font-family: Arial, sans-serif;
  margin: 20px;
  background-color: #fff;
  color: #333;
}

button {
  margin: 5px;
  padding: 8px 12px;
  cursor: pointer;
}

