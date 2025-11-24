# 🎨 CSS Cheat Sheet
![CSS](../../Images/css.webp)

## 🔗 Linking CSS
```css
/* external */
<link rel="stylesheet" href="style.css">

/* internal */
<style>
  body { background: #fafafa; }
</style>

/* inline */
<p style="color: red;">Hello</p>
```

## 🧱 Selectors
```css
element { }
.class { }
#id { }

* { }               /* universal */
div p { }           /* descendant */
div > p { }         /* direct child */
div + p { }         /* adjacent sibling */
div ~ p { }         /* general sibling */

[href] { }          /* attribute */
[href^="https"] { } /* starts-with */
[href$=".jpg"] { }  /* ends-with */
[href*="google"] { }/* contains */
```

## 🎨 Colors
```css
color: red;
color: #ff0099;
color: rgb(255, 0, 153);
color: hsl(320, 100%, 50%);
```

## 🔤 Text
```css
font-family: Arial, sans-serif;
font-size: 20px;
font-weight: bold;
font-style: italic;
text-decoration: underline;
text-align: center;
letter-spacing: 2px;
line-height: 1.5;
```

## 📦 Box Model
```css
width: 200px;
height: 200px;

padding: 20px;
margin: 20px;

border: 2px solid black;
border-radius: 10px;
box-sizing: border-box;
```

## 🧭 Display & Position
```css
display: block;
display: inline;
display: inline-block;
display: flex;
display: grid;
display: none;

position: static;
position: relative;
position: absolute;
position: fixed;
position: sticky;

top: 10px; bottom: 0; left: 0; right: 0;
z-index: 10;
```

## 🧩 Flexbox
```css
display: flex;

flex-direction: row;       /* or column */
justify-content: center;   /* x-axis */
align-items: center;        /* y-axis */
flex-wrap: wrap;
gap: 10px;

flex: 1;
```

## 🟦 Grid
```css
display: grid;
grid-template-columns: repeat(3, 1fr);
grid-template-rows: auto;
gap: 10px;

grid-column: 1 / 3;
grid-row: 2 / 4;
```

## 🎬 Animation
```css
@keyframes spin {
  from { transform: rotate(0); }
  to { transform: rotate(360deg); }
}

.box {
  animation: spin 2s linear infinite;
}
```

## 🌈 Backgrounds
```css
background-color: blue;
background-image: url("bg.jpg");
background-size: cover;
background-repeat: no-repeat;
background-position: center;
```

## 🌪️ Transform & Transition
```css
transform: scale(1.2) rotate(10deg);
transition: all 0.3s ease;
```

## 🧱 Borders & Shadows
```css
border: 2px solid #000;
border-radius: 10px;

box-shadow: 0 4px 10px rgba(0,0,0,0.2);
text-shadow: 2px 2px 5px #000;
```

## 📱 Media Queries
```css
@media (max-width: 600px) {
  body { font-size: 14px; }
}
```

## 🎯 Pseudo Classes & Elements
```css
a:hover { color: red; }
a:focus { outline: 2px solid blue; }
button:disabled { opacity: 0.5; }

p::before { content: "🔥 "; }
p::after { content: " ✨"; }
```

## 🍱 Variables
```css
:root {
  --main-color: #ff0099;
}

h1 {
  color: var(--main-color);
}
```

## 🪟 Overflow
```css
overflow: hidden;
overflow-y: scroll;
```

## 🧼 Reset / Normalize
```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
```
