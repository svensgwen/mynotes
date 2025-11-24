# 🌐 HTML Cheat Sheet

![HTML](../../Images/html.webp)
## 🏷️ Basic Structure
```html
<!DOCTYPE html>
<html>
<head>
  <title>Page Title</title>
  <meta charset="UTF-8">
</head>
<body>
  <h1>Hello World</h1>
</body>
</html>
```

## 🔤 Headings
```html
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
```

## 📝 Text Formatting
```html
<p>Paragraph text</p>
<b>Bold</b>
<strong>Strong</strong>
<i>Italic</i>
<em>Emphasis</em>
<u>Underline</u>
<small>Small</small>
<mark>Highlighted</mark>
```

## 🔗 Links & Images
```html
<a href="https://example.com">Click me</a>
<a href="https://example.com" target="_blank">Open in new tab</a>

<img src="image.jpg" alt="description">
```

## 📃 Lists
### Unordered
```html
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
</ul>
```

### Ordered
```html
<ol>
  <li>Item 1</li>
  <li>Item 2</li>
</ol>
```

### Task-style (not native HTML)
Use checkboxes:
```html
<input type="checkbox" checked> Done<br>
<input type="checkbox"> To do<br>
```

## 🧱 Div & Span
```html
<div>Block container</div>
<span>Inline container</span>
```

## 🎨 Styles
### Inline CSS
```html
<p style="color: red; font-size: 20px;">Styled text</p>
```

### Internal CSS
```html
<style>
  h1 { color: blue; }
</style>
```

## 🧩 Classes & IDs
```html
<div class="box"></div>
<div id="unique"></div>
```

## 📦 Forms
```html
<form action="/submit" method="post">
  <input type="text" name="username">
  <input type="password" name="password">
  <input type="submit" value="Send">
</form>
```

## 🔘 Inputs
```html
<input type="text">
<input type="number">
<input type="email">
<input type="checkbox">
<input type="radio">
<input type="file">
<input type="range">
```

## 🎛️ Select & Textarea
```html
<select>
  <option>Option 1</option>
  <option>Option 2</option>
</select>

<textarea rows="4">Text here</textarea>
```

## 📐 Tables
```html
<table>
  <tr>
    <th>Name</th>
    <th>Age</th>
  </tr>
  <tr>
    <td>John</td>
    <td>22</td>
  </tr>
</table>
```

## 🎬 Media
```html
<video src="movie.mp4" controls></video>
<audio src="audio.mp3" controls></audio>
```

## 🧭 Semantic HTML
```html
<header></header>
<nav></nav>
<section></section>
<article></article>
<aside></aside>
<footer></footer>
```

## ⚡ Script Tag
```html
<script>
  console.log("Hello JS");
</script>
```

## 🔥 Comments
```html
<!-- This is a comment -->
```

## 📁 Linking CSS & JS Files
```html
<link rel="stylesheet" href="style.css">
<script src="script.js"></script>
```

## 🧊 Meta Tags
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="page summary">
```

## 🎯 Buttons
```html
<button>Click</button>
<button disabled>Disabled</button>
```
