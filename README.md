<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fira+Code&display=swap" rel="stylesheet">
<div style="background:#2a2a2a;color:#fff;height:100%;width:100%;font-family: 'Fira Code';padding-left:20px;">
Uploaded On: 08 April 2023 [Saturday]
    
***


# Description

- when you Right-Click then menu open and redirect particular Module.<br/>
👇here, below demonstrated video--check it

***

https://user-images.githubusercontent.com/84908224/230715590-89a3a6cf-31c5-4597-86de-4bf21698d7b3.mp4

***

Here I shared about used technologies,frameworks and so on...

<details>

https://user-images.githubusercontent.com/84908224/230715410-9292cdd6-6d33-4910-a091-9567bd45b48e.mp4


    <summary> Technologies </summary>

***

- [HTML](http://www.w3schools.com/html/default.asp) - A markup language for describing web documents.

- [CSS](http://www.w3schools.com/css/default.asp) - A style sheet language used for describing the look and formatting of a document written in a markup language.

- [Java Script](http://www.w3schools.com/js/default.asp) - A programming language of the Web.

- [Font Awesome](https://fontawesome.com/) - Font Awesome is the Internet's icon library and toolkit, used by millions of designers, developers, and content creators.

- [cdnjs](https://cdnjs.com/) - cdnjs is a free and open-source software content delivery network hosted by Cloudflare. 
<hr/>
</details>

<details>

<summary> Source Code </summary>

index.html
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Right Click Event</title>
    <link rel="stylesheet" href="style.css" />
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.1.1/css/all.min.css"/>
  </head>

  <body>
    <div id="container" class="container">
      <div class="menu" id="menu">
        <button class="btn" id="btn"><i class="fa-solid fa-xmark"></i></button>
        <a href="#Home" class="links">Home</a>
        <a href="#About" class="links">About</a>
        <a href="#Services" class="links">Services</a>
        <a href="#Contact" class="links">Contact</a>
      </div>
      <div id="Home" class="box">Home</div>
      <div id="About" class="box">About</div>
      <div id="Services" class="box">Services</div>
      <div id="Contact" class="box">Contact</div>
      <div class="overlay" id="overlay"></div>
      <h4>Developed By Tirth</h4>
    </div>

    <script src="index.js"></script>
  </body>
</html>
```
style.css
```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Poppins", sans-serif;
  scroll-behavior: smooth;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}
body {
  overflow-x: hidden;
}
.container {
  width: 100%;
  height: 100vh;
  overflow-y: auto;
}
.overlay {
  width: 100%;
  height: 100vh;
  background: #000000ac;
  backdrop-filter: blur(10px);
  position: fixed;
  top: 0;
  left: 0;
  display: none;
}
.menu {
  background: #000;
  position: absolute;
  display: none;
  z-index: 5000;
  flex-direction: column;
  border-radius: 10px;
  text-align: center;
  overflow: hidden;
}
.menu .btn {
  border: none;
  font-size: 1.2em;
  cursor: pointer;
}
.menu a {
  text-decoration: none;
  color: #fff;
  padding: 5px 35px;
}
.menu a:hover {
  background: #181818;
}
.box {
  width: 100%;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 5em;
  color: #fff;
}
.box:nth-child(2) {
  background: #751c59;
}
.box:nth-child(3) {
  background: #ffbf34;
}
.box:nth-child(4) {
  background: #11684c;
}
.box:nth-child(5) {
  background: #e9253c;
}


::-webkit-scrollbar-track {
  -webkit-box-shadow: inset 0 0 6px rgba(0, 0, 0, 0.3);
  background-color: #f5f5f5;
}

::-webkit-scrollbar {
  width: 10px;
  background-color: #f5f5f5;
}

::-webkit-scrollbar-thumb {
  background-color: #000000;
  border: 2px solid #555555;
}
```
index.js
```js
const container = document.querySelector("#container");
const btn = document.querySelector("#btn");
const links = document.querySelectorAll(".links");

container.addEventListener("contextmenu", handleClick);
btn.addEventListener("click", handleClick);
links.forEach((e) => {
  e.addEventListener("click", handleClick);
});

function handleClick(e) {
  const menu = document.getElementById("menu");
  const overlay = document.getElementById("overlay");
  if (e.which === 3) {
    e.preventDefault();
    overlay.style.display = "block";
    menu.style.display = "flex";
    menu.style.opacity = "1";
    menu.style.transform = `translate(${e.clientX}px, ${e.clientY}px) scale(1)`;
  } else if (e.which === 1) {
    overlay.style.display = "none";
    menu.style.display = "none";
  }
}
```

</details>


*[Back to top](#description)*

<br/>
<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&pause=1000&color=1600F7&background=FFFFFF&center=true&vCenter=true&width=435&lines=Always+Learn+New+Things!+Keep+It+Up;Thank+You+%F0%9F%99%8F;Visit+Again...+%E2%9D%A4%EF%B8%8F" alt="Typing SVG" />

</div>
