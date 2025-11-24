# 🟩 Pug (HTML Templating) Cheat Sheet

![PUG HTML](../../Images/pughtml.webp)

## 🚀 Basic Template
```pug
doctype html
html
  head
    title My Page
  body
    h1 Hello Pug
    p This is a paragraph
```

## 🧱 Tags
```pug
h1 Heading
p Paragraph text
div.container
span.label
```

## 🎯 IDs & Classes
```pug
#main
.container
.card.large
div#app.container
```

## ✍️ Text
```pug
p This is text
p.
  Multiline text block
  continues here...
```

## 🔗 Links & Images
```pug
a(href="/home") Home
img(src="img.png" alt="image")
```

## 📦 Attributes
```pug
input(type="text" placeholder="Name")
button(disabled) Can't click
```

## 🧩 Variables (Interpolation)
```pug
p Hello #{name}
p #{user.age} years old
```

## 🧠 JS Expressions
```pug
p= username
p= count + 1
```

## 🔁 Each Loop
```pug
ul
  each item in items
    li= item
```

With index:
```pug
each val, i in list
  p #{i}: #{val}
```

## 🧱 Conditionals
```pug
if loggedIn
  p Welcome back!
else
  p Please log in.
```

Else-if:
```pug
if score > 90
  p A+
else if score > 80
  p A
else
  p Keep trying
```

## 🗂️ Includes
```pug
include header.pug
include components/card.pug
```

## 📁 Extends & Blocks
### Base Layout (`layout.pug`)
```pug
doctype html
html
  head
    block head
  body
    block content
```

### Page
```pug
extends layout.pug

block head
  title Home Page

block content
  h1 Welcome
  p This is the homepage.
```

## 🧱 Mixins (Reusable Components)
```pug
mixin card(title, text)
  .card
    h2= title
    p= text
```

Usage:
```pug
+card("Hello", "Welcome to the card")
```

## 🔌 Inline JS
```pug
script.
  console.log("hello")
```

## 🧼 Comments
```pug
// regular comment
//- won't show in HTML
```

## 🎨 Styles
```pug
style.
  body { background: #222; }
```

## 🎯 Doctype Shortcuts
```pug
doctype html
doctype xml
```

## 🧪 Boolean Attributes
```pug
input(type="checkbox" checked)
```

## 🌐 HTML Equivalents (Quick Map)
```pug
div#app            ← <div id="app">
div.item.big       ← <div class="item big">
a(href="/") Home   ← <a href="/">Home</a>
p Hello #{name}    ← <p>Hello NAME</p>
```
