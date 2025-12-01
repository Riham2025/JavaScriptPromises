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


## 🛠 Creating a Promise

```js
const myPromise = new Promise((resolve, reject) => {
    
    let success = true;

    if (success) {
        resolve("Operation successful!");
    } else {
        reject("Error occurred!");
    }
});


```

     
    
resolve() → The Promise succeeded

reject() → The Promise failed

---

🔥 Handling Promises (then, catch, finally)

```
myPromise
  .then(result => console.log("Success:", result))
  .catch(error => console.log("Error:", error))
  .finally(() => console.log("Completed."));
```

| Method       | Runs When          |
| ------------ | ------------------ |
| `.then()`    | Promise fulfilled  |
| `.catch()`   | Promise rejected   |
| `.finally()` | Runs in every case |



```
let uploadVideo = new Promise((resolve, reject) => {
    let completed;

    // do some async operations....
    completed = true;
     //completed = false;

    if (completed) {
        resolve("Successfully Uploaded.");
    }
    else {
        reject("Sorry, Failed !!!");
    }
});

uploadVideo
    .then(msg => {
        console.log("then is called: " + msg);
    })
    .catch(msg => {
        console.log("catch is called: " + msg);
    });

    ```