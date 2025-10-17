# 📝 To-Do CRUD

## 🧩 Overview

This project is part of the **JavaScript hands-on learning series**.
It demonstrates a complete **CRUD (Create, Read, Update, Delete)** flow for a simple **To-Do List Application**, built using **HTML, CSS, and JavaScript** — without using any loops for rendering.

The app stores data in both **LocalStorage** (for offline persistence) and an external temporary backend, **CrudCrud API**, to simulate real database operations.
It also introduces the concept of using **recursion** to display data instead of traditional loops.

---

## 🧠 What is CRUD?

**CRUD** stands for:

* **C – Create:** Add new data or items (e.g., a new task)
* **R – Read:** Retrieve and display data (e.g., list all tasks)
* **U – Update:** Modify existing data (e.g., edit a task)
* **D – Delete:** Remove data (e.g., delete a task)

CRUD operations form the backbone of most web applications, allowing dynamic interaction with databases or storage.

---

## 🧠 How CrudCrud API Helps

**CrudCrud** is a free, temporary REST API used to simulate a real backend without setting up a server.

It allows the app to perform **CRUD operations over HTTP**:

| Operation  | Example Use in App                                          |
| ---------- | ----------------------------------------------------------- |
| **POST**   | Add a new task to the backend when a user clicks “Add Task” |
| **GET**    | Fetch all tasks from the backend on page load               |
| **PUT**    | Update a task’s content when a user clicks “Update”         |
| **DELETE** | Remove a task from the backend when a user clicks “Delete”  |

> ⚠️ **Note:** Data on CrudCrud is **temporary** and resets every 24 hours. It’s perfect for testing and learning CRUD without a full backend setup.

---

## 🧠 Learning Objectives

This project helps learners understand:

### Core CRUD Logic

* Create, Read, Update, and Delete tasks dynamically
* Understand how user actions affect both UI and stored data

### LocalStorage Integration

* Store and retrieve data from the browser
* Keep data even after refreshing the page

### Backend Simulation via API

* Connect to a mock backend using the **CrudCrud REST API**
* Learn how to use `fetch()` for **POST, PUT, and DELETE** requests

### Recursion Concept

* Replace traditional loops (`for`, `while`) with recursive function calls
* Understand **base** and **recursive conditions** through real implementation

### DOM Manipulation

* Dynamically create HTML elements for tasks
* Handle events like button clicks for update/delete actions

---

## 🧱 Project Structure

```
todo-crud/
├── index.html          # Main structure of the web app
├── style.css           # Styling for the To-Do app
├── script.js           # JavaScript logic for CRUD + recursion
└── README.md           # Project documentation
```

| File       | Description                                                               |
| ---------- | ------------------------------------------------------------------------- |
| index.html | Contains the page layout and links to `style.css` & `script.js`           |
| style.css  | Defines styling for input boxes, buttons, and task list UI                |
| script.js  | Implements all CRUD logic, recursion-based display, and API communication |
| README.md  | Guide explaining how to run and understand the project                    |

---

## 🏷️ Technologies Used

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge\&logo=html5\&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge\&logo=css3\&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge\&logo=javascript\&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![CrudCrud API](https://img.shields.io/badge/CrudCrud_API-008080?style=for-the-badge)](https://crudcrud.com/)
[![LocalStorage](https://img.shields.io/badge/LocalStorage-FFA500?style=for-the-badge)](https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage)

---

## ⚙️ How the App Works

### Page Load

* Tasks are automatically loaded from **LocalStorage** using recursion

### Add a Task

* Type a new task and click **“Add Task”**
* Task is displayed on screen, saved to **LocalStorage**, and sent to CrudCrud via **POST request**

### Update a Task

* Click **“Update”** → enter new text in a prompt
* Change is updated locally and via **PUT request** on CrudCrud

### Delete a Task

* Click **“Delete”** → removes the task from **DOM**, **LocalStorage**, and CrudCrud via **DELETE request**

### Recursive Rendering

* Instead of using loops, tasks are displayed one by one using a recursive function:

```javascript
displayTaskRecursively(index);
```

---

## 💻 Technologies Summary

| Category     | Technology              |
| ------------ | ----------------------- |
| Frontend     | HTML5, CSS3, JavaScript |
| Backend API  | CrudCrud REST API       |
| Storage      | LocalStorage            |
| Logic Type   | Recursion (no loops)    |
| HTTP Methods | GET, POST, PUT, DELETE  |

---

## 📚 Key Learning Takeaways

✅ CRUD operation flow in real web apps
✅ Working with asynchronous JavaScript (`async / await`)
✅ Using **LocalStorage** for persistence
✅ Understanding **recursion** practically
✅ Clean **UI & DOM** event handling
✅ Integrating frontend logic with an external API

---

## 🧰 Developer Tips

* Check your **Browser Console → Network Tab** to see live API requests
* CrudCrud data is **temporary** — it automatically resets every 24 hours
* You can freely modify the `API_URL` constant in `script.js` with your own CrudCrud endpoint
* This is a **no-loop challenge**, so focus on understanding how recursion works in task rendering
