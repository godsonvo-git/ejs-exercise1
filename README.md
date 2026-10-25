# 📅 Weekday Warrior (EJS Exercise)

> A simple Express + EJS practice project that detects the current day and displays a motivational message — work hard on weekdays, have fun on weekends!

---

![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white)
![EJS](https://img.shields.io/badge/EJS-B4CA65?style=for-the-badge&logo=ejs&logoColor=black)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

---

## ✨ Overview

**Weekday Warrior** is a beginner-friendly Node.js project created to practice **EJS templating** with Express.

The app checks the current day of the week and renders a dynamic message:

- **Weekdays** → “Hey It's a weekday, It's time to work hard!”
- **Weekends** → “Hey It's the weekend, It's time to have some fun!”

It demonstrates how to pass data from the server to an EJS template and render dynamic content.

---

## 🚀 Features

- 📆 Detects the current day using JavaScript `Date` object
- 🧠 Conditional logic for weekday vs weekend
- 📄 Server-side rendering with EJS
- 🔄 Dynamic content passed from Express to the template
- ⚡ Lightweight Express server
- 🖥️ Simple and clean HTML output

---

## 🛠️ Technologies Used

| Technology     | Purpose                                      |
|----------------|----------------------------------------------|
| **Node.js**    | JavaScript runtime environment               |
| **Express**    | Web server and routing                       |
| **EJS**        | Embedded JavaScript templating engine        |
| **JavaScript** | Day detection logic and server-side code     |

---

## 🧠 Concepts Practiced

### Express Basics
- Creating an Express app
- Setting up a simple route (`GET /`)
- Starting a local server on port 3000

### EJS Templating
- Rendering an EJS template with `res.render()`
- Passing data from the server to the view
- Using EJS output tags (`<%= %>`)

### JavaScript Fundamentals
- Working with the `Date` object
- `getDay()` method
- Conditional statements (`if`)
- Template literals and dynamic strings

---

## 🔢 How the Logic Works

```javascript
const today = new Date();
const day = today.getDay();   // 0 = Sunday, 6 = Saturday

let type = "a weekday";
let adv = "It's time to work hard";

if (day === 0 || day === 6) {
  type = "the weekend";
  adv = "It's time to have some fun";
}

res.render("index.ejs", {
  dayType: type,
  advice: adv,
});
```
## EJS Template Output
```
<h1>Hey It's <%= dayType %>, <%= advice %>!</h1>
```
## 📂 Project Structure
```
ejs-exercise1/
│
├── views/
│   └── index.ejs
│
├── index.js
├── package.json
├── package-lock.json
└── README.md
```
## ⚙️ Running the Project Locally
#### 1. Clone the repository
```
git clone https://github.com/godsonvo-git/ejs-exercise1.git
```
#### 2. Navigate into the project
```
cd ejs-exercise1
```
#### 3. Install dependencies
```
npm install
```
#### 4. Start the server
```
node index.js
```
#### 5. Open in your browser
```
Visit: http://localhost:3000
```
## 🎯 Learning Goals
The main goals of this project were to practice:
- Setting up a basic Express server
- Using EJS as a view engine
- Passing dynamic data to templates
- Working with the JavaScript Date object
- Writing conditional logic on the server
- Understanding server-side rendering (SSR)

---

## 👨‍💻 Author

**Godson V O**

* 🌐 [Portfolio](https://godsonvo-portfolio.vercel.app/)
* 💻 [GitHub](https://github.com/godsonvo-git)
* 🔗 [LinkedIn](https://www.linkedin.com/in/godsonvo/)

---
<div align="center">

### ⭐ If you found this project useful, consider giving the repository a star!

</div>