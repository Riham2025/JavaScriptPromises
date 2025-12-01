# 📌 JavaScript Promises – Fundamentals + Full Practical Task

This documentation explains **JavaScript Promises** in a clear, structured way with examples, visuals, and a fully solved task.  
The goal is to help you understand how Promises work, why they exist, and how to use them in real development.

---

## 🔥 What is a Promise?

A **Promise** in JavaScript represents a result that will be available **in the future**, not immediately.  
Promises are mainly used for **asynchronous operations**,*, such as:

| Operation Type | Example |
|---|---|
| Network/API request | Fetching user data |
| Time-based tasks | setTimeout() |
| File handling | Loading images, reading files |
| I/O operations | Database access |


Instead of stopping code execution, JavaScript continues running and **fulfills** the promise later.

---


## 📍 Promise States

Every Promise has **three possible states**:

| State | Meaning |
|---|---|
| `Pending` | Promise still running & waiting |
| `Fulfilled` | Operation completed successfully (`resolve`) |
| `Rejected` | Operation failed (`reject`) |

Once a Promise changes from *Pending* → *Fulfilled/Rejected*, it never changes again.

---