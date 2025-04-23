# 🎯 JavaScript Event Handling & Interactive Elements Assignment

Welcome to the **ultimate JavaScript playground**! 🎉 This assignment is where we turn boring web pages into dynamic, responsive, *alive* experiences. Get ready to master **event handling**, build **interactive components**, and validate forms like a pro! 💪

## 📁 Assignment Structure

```
📂 js-event-assignment/
├── index.html         # Your playground – where it all comes together
├── style.css          # Keep it cute (optional but encouraged)
└── script.js          # The JavaScript wizardry happens here
```

---

## 🧪 What to Build

Here’s what your interactive bundle of joy should include:

### 1. Event Handling 🎈  
- Button click ✅  
- Hover effects ✅  
- Keypress detection ✅  
- Bonus: A secret action for a *double-click* or *long press* 🤫

### 2. Interactive Elements 🎮  
- A button that changes text or color  
- An image gallery or slideshow  
- Tabs or accordion-style content  
- Bonus: Add some animation using JS or CSS ✨

### 3. Form Validation 📋✅  
- Required field checks  
- Email format validation  
- Password rules (e.g., min 8 characters)  
- Bonus: Real-time feedback while typing

---

## 🧙‍♂️ Pro Tips

- Keep your code clean and commented – your future self will thank you!
- Think about **user experience** – what makes your site more *fun* to use?
- Don’t be afraid to **Google and experiment** – that’s how real developers roll!


<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Interactive Webpage</title>
  <style>
    /* Basic Styling */
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      padding: 20px;
    }
    button {
      padding: 10px 20px;
      margin: 10px;
      font-size: 16px;
      cursor: pointer;
    }
    .tabContent {
      display: none;
      padding: 20px;
      margin-top: 10px;
      border: 1px solid #ccc;
      transition: all 0.3s ease-in-out;
    }
    .tabContent.show {
      display: block;
      opacity: 1;
    }
    .tabContent.hide {
      opacity: 0;
    }
    #gallery img {
      width: 300px;
      height: auto;
      transition: transform 0.3s;
    }
    #gallery img:hover {
      transform: scale(1.1);
    }
    input, span {
      margin: 10px;
      padding: 10px;
    }
    #feedback {
      font-weight: bold;
    }
  </style>
</head>
<body>

  <!-- Event Handling Section -->
  <h2>Event Handling 🎈</h2>
  <button id="clickButton">Click Me!</button>
  <br>
  <button id="hoverButton">Hover Over Me!</button>
  <br>
  <input type="text" id="inputField" placeholder="Press any key...">
  <br>
  <div id="secretDiv">Double-click me for a secret action!</div>
  
  <hr>

  <!-- Interactive Elements -->
  <h2>Interactive Elements 🎮</h2>
  <button id="changeTextButton">Click to Change Text</button>
  <br><br>
  <div id="gallery">
    <img id="slideImage" src="https://via.placeholder.com/300" alt="Slide 1">
    <button onclick="nextImage()">Next Image</button>
  </div>
  <br>
  <div class="tabs">
    <button class="tabButton" onclick="showTab(0)">Tab 1</button>
    <button class="tabButton" onclick="showTab(1)">Tab 2</button>
    <div id="content1" class="tabContent">Content for Tab 1</div>
    <div id="content2" class="tabContent">Content for Tab 2</div>
  </div>
  
  <hr>

  <!-- Form Validation Section -->
  <h2>Form Validation 📋✅</h2>
  <form id="myForm">
    <input type="text" id="name" required placeholder="Enter your name">
    <br>
    <input type="email" id="email" required placeholder="Enter your email">
    <br>
    <input type="password" id="password" required placeholder="Enter your password">
    <br>
    <button type="submit">Submit</button>
  </form>
  <br>
  <input type="text" id="username" placeholder="Username">
  <span id="feedback"></span>

  <script>
    // Event Handling

    // Button Click
    document.getElementById("clickButton").addEventListener("click", function() {
      alert("Button clicked!");
    });

    // Hover Effects
    document.getElementById("hoverButton").addEventListener("mouseenter", function() {
      this.style.backgroundColor = "lightblue";
    });
    document.getElementById("hoverButton").addEventListener("mouseleave", function() {
      this.style.backgroundColor = "";
    });

    // Keypress Detection
    document.getElementById("inputField").addEventListener("keypress", function(event) {
      console.log("Key pressed: " + event.key);
    });

    // Secret Action (Double-click and Long press)
    document.getElementById("secretDiv").addEventListener("dblclick", function() {
      alert("You found the secret action!");
    });

    let timer;
    document.getElementById("secretDiv").addEventListener("mousedown", function() {
      timer = setTimeout(function() {
        alert("Long press detected!");
      }, 1000);
    });

    document.getElementById("secretDiv").addEventListener("mouseup", function() {
      clearTimeout(timer);
    });

    // Interactive Elements

    // Button that Changes Text or Color
    document.getElementById("changeTextButton").addEventListener("click", function() {
      this.textContent = "Text Changed!";
      this.style.backgroundColor = "green";
    });

    // Image Gallery/Slideshow
    const images = ["https://via.placeholder.com/300", "https://via.placeholder.com/300/0000FF", "https://via.placeholder.com/300/FF0000"];
    let currentIndex = 0;

    function nextImage() {
      currentIndex = (currentIndex + 1) % images.length;
      document.getElementById("slideImage").src = images[currentIndex];
    }

    // Tabs/Accordion-style Content
    function showTab(index) {
      const allContent = document.querySelectorAll(".tabContent");
      allContent.forEach(content => content.style.display = "none");

---

## 🎉 Now Go Make It Fun!

Remember – this isn't just code. It's your **first step toward creating magical user experiences**. So play around, break stuff (then fix it), and most of all, have FUN! 😄

Happy Coding! 💻✨  
