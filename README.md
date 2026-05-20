# Ex03 To-Do List using JavaScript
## Date:

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
```
##index.html


<!DOCTYPE html>
<html>
<head>
    <title>To-Do App</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<div class="container">
    <h1>To-Do List</h1>

    <input type="text" id="taskInput" placeholder="Enter a task">
    <button onclick="addTask()">Add</button>

    <ul id="taskList"></ul>
</div>

<script src="script.js"></script>

</body>
</html>


##style.css


body {
    font-family: Arial, sans-serif;
    background-color: #f2f2f2;
    display: flex;
    justify-content: center;
    margin-top: 50px;
}

.container {
    background: white;
    padding: 20px;
    width: 350px;
    border-radius: 10px;
    box-shadow: 0 0 10px gray;
}

h1 {
    text-align: center;
}

input {
    width: 70%;
    padding: 10px;
}

button {
    padding: 10px;
    cursor: pointer;
}

ul {
    list-style: none;
    padding: 0;
}

li {
    background: #e6e6e6;
    margin-top: 10px;
    padding: 10px;
    display: flex;
    justify-content: space-between;
}

.completed {
    text-decoration: line-through;
    color: gray;
}



##script.js


let taskList = document.getElementById("taskList");

function addTask() {
    let taskInput = document.getElementById("taskInput");
    let taskText = taskInput.value;

    if (taskText === "") {
        alert("Please enter a task");
        return;
    }

    let li = document.createElement("li");

    let span = document.createElement("span");
    span.textContent = taskText;

    span.onclick = function () {
        span.classList.toggle("completed");
    };

    let deleteBtn = document.createElement("button");
    deleteBtn.textContent = "Delete";

    deleteBtn.onclick = function () {
        li.remove();
    };

    li.appendChild(span);
    li.appendChild(deleteBtn);

    taskList.appendChild(li);

    taskInput.value = "";
}
```


## OUTPUT

<img width="1902" height="980" alt="Screenshot 2026-05-20 113432" src="https://github.com/user-attachments/assets/cf67f21b-a112-4011-a167-04e7a0270533" />

## RESULT
The program for creating To-do list using JavaScript is executed successfully.

