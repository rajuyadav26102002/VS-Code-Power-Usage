# VS-Code-Power-Usage

# ✨ Emmet Abbreviations in VS Code

Emmet is a powerful tool built into VS Code that helps you **write HTML and CSS faster** using short expressions (abbreviations) that expand into full code.

---

## 📌 What is Emmet?
- Emmet is like **shortcuts for coding**.
- Instead of writing full HTML/CSS manually, you write abbreviations and press **Tab** to expand.

---

## ❓ Why use Emmet?
- 🚀 Speeds up development.  
- ✍️ Reduces repetitive typing.  
- ✅ Ensures cleaner and consistent code.  
- 🔍 Improves focus on structure, not boilerplate.  

---

## 🎯 How to Use Emmet in VS Code
1. Open any `.html` or `.css` file in VS Code.  
2. Type an **abbreviation**.  
3. Press **Tab** → it expands into code.  

⚡ Tip: Make sure **Emmet: Trigger Expansion On Tab** is enabled in VS Code settings.

---

# Emmet Abbreviation Example

## Basic HTML Boilerplate

**Expands to:**
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>
  
</body>
</html>
```
## 2. Unordered List with Items

**Abbreviation**
- ul>li*3
  
**Expands to**
```html
<ul>
  <li></li>
  <li></li>
  <li></li>
</ul>
```

## 3. Navigation with Links

**Abbreviation**
- nav>ul>li*3>a{Link $}

**Expands to**
```html
<nav>
  <ul>
    <li><a>Link 1</a></li>
    <li><a>Link 2</a></li>
    <li><a>Link 3</a></li>
  </ul>
</nav>
```

## 4. Repeated Cards with Content

**Abbreviation**

- .card*2>h3{Title $}+p>lorem10


**Expands to**
```html
<div class="card">
  <h3>Title 1</h3>
  <p>Lorem ipsum dolor sit amet...</p>
</div>
<div class="card">
  <h3>Title 2</h3>
  <p>Lorem ipsum dolor sit amet...</p>
</div>
```

5. Simple Login Form

**Abbreviation**

- form>input:text+input:password+button{Login}

**Expands to**
```html

<form>
  <input type="text">
  <input type="password">
  <button>Login</button>
</form>

6. Table with Rows & Columns

Abbreviation

table>thead>tr>th*3{Col $}^^tbody>tr*2>td*3{Item}
```
6. Table with Rows & Columns

**Abbreviation**

- table>thead>tr>th*3{Col $}^^tbody>tr*2>td*3{Item}

**Expands to**
```html

<table>
  <thead>
    <tr>
      <th>Col 1</th>
      <th>Col 2</th>
      <th>Col 3</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Item</td>
      <td>Item</td>
      <td>Item</td>
    </tr>
    <tr>
      <td>Item</td>
      <td>Item</td>
      <td>Item</td>
    </tr>
  </tbody>
</table>
```


# 📝 User Snippet – HTML Boilerplate in VS Code

## 🔍 What is a User Snippet?
A **user snippet** in VS Code is a reusable block of code you can trigger with a short keyword.  
Instead of typing the same boilerplate again and again, you just type a small prefix → press **Tab** → and the full code expands.

---

## 🎯 Why Important?
- 🚀 **Saves time** – no need to type boilerplate manually.  
- ✅ **Consistency** – always start with the same structure.  
- 🎨 **Customizable** – add your own CSS/JS setup.  

---

## ⚙️ How to Create a User Snippet (Step by Step)

1. Open **Command Palette**  
   - `Ctrl + Shift + P` 

2. Search **Preferences: Configure User Snippets**

3. Select **html.json** (for HTML files)

4. Paste this code:

```json
{
  "HTML5 Boilerplate": {
    "prefix": "html5",
    "body": [
      "<!DOCTYPE html>",
      "<html lang=\"en\">",
      "<head>",
      "  <meta charset=\"UTF-8\">",
      "  <meta name=\"viewport\" content=\"width=device-width, initial-scale=1.0\">",
      "  <title>$1</title>",
      "</head>",
      "<body>",
      "  $2",
      "</body>",
      "</html>"
    ],
    "description": "Custom HTML5 boilerplate"
  }
}
```
# Emmet Expansion Example

## ✅ Example Output

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Page</title>
</head>
<body>
  <!-- Content goes here -->
</body>
</html>
```
# 🎯 Learning Outcomes

- Learned what a user snippet is and why it’s useful.  
- Understood how to create and use a snippet in VS Code.  
- Practiced boosting productivity with custom boilerplate code.

# 🐞 Walkthrough: Basic JavaScript Debugging in VS Code

## 🔍 What is Debugging?
Debugging is the process of **finding and fixing errors (bugs)** in your code.  
In VS Code, you can run JavaScript step by step, check variable values, and pause execution using **breakpoints**.

---

## 🎯 Why Debugging in VS Code?
- 🛑 Set **breakpoints** → pause code at specific lines.  
- 👀 Inspect **variables and values** in real time.  
- ⏩ Step through code → line by line.  
- ⚡ Faster than just using `console.log()` everywhere.  

---

## ⚙️ Setup Debugging in VS Code

1. **Install Node.js** (required to run JavaScript outside the browser).  
   - Check: `node -v`

2. **Open your project folder** in VS Code.  

3. **Create a Debug Configuration**  
   - Go to **Run and Debug** (sidebar or press `Ctrl + Shift + D`).  
   - Click **create a launch.json file** → choose **Node.js**.  

4. VS Code will create a `.vscode/launch.json` file. Example:

```json
{
  "version": "0.2.0",
  "configurations": [
    {
      "type": "node",
      "request": "launch",
      "name": "Run JavaScript File",
      "program": "${file}"
    }
  ]
}
```



## 📝 Example: Code to Debug
```javascript
let x = 5;
let y = 10;

let total = x + y; // breakpoint here
console.log("The total is:", total);
```

## 🔍 How to Debug This

1. Open this file in VS Code (e.g., `app.js`).  
2. Click **left of line 4** (`let total = x + y;`) → a red dot appears (**breakpoint**).  
3. Press **F5** → code runs and **pauses at the breakpoint**.  
4. Check variables **x**, **y**, and **total** in the **Variables panel**.  
5. Press **F10 (Step Over)** → move to the next line and see the output in the **Debug Console**.  

---

## 🎯 🎯 Learning Outcomes
- 🛑 How to **set a breakpoint** in VS Code.  
- ▶️ How to **run and pause code** using the debugger.  
- 👀 How to **inspect variable values** while debugging.  

## 📚 Resources

- [📘 Emmet Cheat Sheet](https://docs.emmet.io/cheat-sheet/) – Quick reference for Emmet abbreviations.  
- [📝 VS Code Snippets](https://code.visualstudio.com/docs/editor/userdefinedsnippets) – Guide to creating and managing custom snippets.  
- [🐞 VS Code Debugging](https://code.visualstudio.com/docs/editor/debugging) – Official docs for debugging JavaScript and other languages in VS Code.  
