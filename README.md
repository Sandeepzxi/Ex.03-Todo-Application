# Ex03 To-Do List using JavaScript
## Date:03.10.2025

## AIM
To create a To-do Application with all features using JavaScript.

## ALGORITHM
### STEP 1
Build the HTML structure (index.html).

### STEP 2
Style the App (style.css).

### STEP 3
Plan the features the To-Do App should have.

### STEP 4
Create a To-do application using Javascript.

### STEP 5
Add functionalities.

### STEP 6
Test the App.

### STEP 7
Open the HTML file in a browser to check layout and functionality.

### STEP 8
Fix styling issues and refine content placement.

### STEP 9
Deploy the website.

### STEP 10
Upload to GitHub Pages for free hosting.

## PROGRAM

# Index.html

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Todo App</title>
  <link rel="stylesheet" href="index.css">
</head>
<body>
  <div class="todo-container">
    <h1>💡 Todo application</h1>
    <div class="input-section">
      <input type="text" id="taskInput" placeholder="Type your task here...">
      <button onclick="addTask()">Add</button>
    </div>
    <ul id="taskList"></ul>
  </div>

  <script src="index.js"></script>
</body>
</html>

```
# Index.js
````
function addTask() {
  const input = document.getElementById("taskInput");
  const taskText = input.value.trim();
  if (!taskText) return;

  const li = document.createElement("li");
  li.innerHTML = `
    <span onclick="toggleComplete(this)">${taskText}</span>
    <button onclick="deleteTask(this)">Delete</button>
  `;
  document.getElementById("taskList").appendChild(li);
  input.value = "";
}

function deleteTask(button) {
  button.parentElement.remove();
}

function toggleComplete(span) {
  span.parentElement.classList.toggle("completed");
}

````
# Index.css
```
/* Body and container */
body {
  font-family: 'Arial', sans-serif;
  background: #0f0f0f;
  display: flex;
  justify-content: center;
  align-items: flex-start;
  min-height: 100vh;
  padding-top: 60px;
  color: #fff;
}

.todo-container {
  background: rgba(0,0,0,0.6);
  padding: 30px;
  border-radius: 25px;
  width: 90%;
  max-width: 450px;
  box-shadow: 0 0 40px #00ffff, 0 0 20px #ff00ff inset;
  border: 1px solid #0ff;
  backdrop-filter: blur(10px);
}

/* Header */
h1 {
  text-align: center;
  margin-bottom: 25px;
  color: #00ffff;
  text-shadow: 0 0 5px #0ff, 0 0 10px #0ff;
  letter-spacing: 1px;
}

/* Input section */
.input-section {
  display: flex;
  gap: 10px;
  margin-bottom: 20px;
}

input[type="text"] {
  flex: 1;
  padding: 12px;
  border-radius: 15px;
  border: 2px solid #0ff;
  outline: none;
  background: rgba(255,255,255,0.05);
  color: #fff;
  font-size: 16px;
  box-shadow: 0 0 10px #0ff;
  transition: 0.3s;
}

input[type="text"]:focus {
  border-color: #ff00ff;
  box-shadow: 0 0 15px #ff00ff;
}

button {
  padding: 12px 20px;
  border-radius: 15px;
  border: none;
  cursor: pointer;
  font-weight: bold;
  background: linear-gradient(90deg, #ff00ff, #00ffff);
  color: #000;
  transition: 0.3s;
}

button:hover {
  transform: scale(1.05);
  box-shadow: 0 0 15px #ff00ff, 0 0 15px #0ff inset;
}

/* Task list */
ul {
  list-style: none;
  padding: 0;
}

li {
  background: rgba(255,255,255,0.05);
  margin-bottom: 15px;
  padding: 15px;
  border-radius: 15px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: #fff;
  font-weight: 500;
  border-left: 4px solid #00ffff;
  transition: 0.2s;
}

li:hover {
  transform: scale(1.02);
  box-shadow: 0 0 10px #00ffff;
}

li.completed {
  text-decoration: line-through;
  color: #888;
  border-left: 4px solid #ff00ff;
}

li button {
  background: #ff00ff;
  padding: 6px 12px;
  border-radius: 10px;
  font-weight: bold;
  border: none;
  cursor: pointer;
  transition: 0.3s;
}

li button:hover {
  transform: scale(1.1);
  background: #ff66ff;
}

```

## OUTPUT

<img width="1919" height="1078" alt="image" src="https://github.com/user-attachments/assets/ec7dd621-8728-4c27-a255-9eac92e91a1c" />

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/b6417310-06f4-48d4-b141-a93dae98dc69" />


## RESULT
The program for creating To-do list using JavaScript is executed successfully.
