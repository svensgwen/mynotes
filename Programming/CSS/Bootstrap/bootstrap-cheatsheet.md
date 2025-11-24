# 💙 Bootstrap 5.x Cheat Sheet — Modern Essentials
![Bootstrap](../../../Images/bootstrap.webp)

## 🚀 CDN
```html
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
```

---

# 🎨 Layout System

## 📦 Container
```html
<div class="container">...</div>
<div class="container-fluid">...</div>
<div class="container-lg">...</div>
```

## 🧱 Grid Basics
```html
<div class="row">
  <div class="col">A</div>
  <div class="col">B</div>
</div>
```

## 🔢 Column Sizes
```html
<div class="col-6 col-md-4 col-lg-3"></div>
```

## 📐 Breakpoints
```
sm  ≥ 576px
md  ≥ 768px
lg  ≥ 992px
xl  ≥ 1200px
xxl ≥ 1400px
```

---

# 🎛️ Utilities (Massively Important)

## 📏 Spacing
```html
mt-3   mb-2    mx-auto
p-3    py-4    px-2
```

## 🧲 Flexbox
```html
d-flex
justify-content-center
align-items-center
flex-column
```

## 🧩 Display Helpers
```html
d-block
d-none
d-md-block
```

## 🎨 Colors
```html
text-primary
bg-dark text-white
```

## 🖼️ Borders
```html
border
border-0
rounded
rounded-circle
```

## 🗂️ Shadows
```html
shadow
shadow-sm
shadow-lg
```

---

# 🧱 Components

## 🔘 Buttons
```html
<button class="btn btn-primary">Blue</button>
<button class="btn btn-outline-danger">Outline</button>
```

## 📦 Cards
```html
<div class="card" style="width:18rem;">
  <img src="img.jpg" class="card-img-top">
  <div class="card-body">
    <h5 class="card-title">Card</h5>
    <p class="card-text">...</p>
    <a href="#" class="btn btn-primary">Go</a>
  </div>
</div>
```

## 📰 Navbar
```html
<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
  <div class="container-fluid">
    <a class="navbar-brand">Brand</a>
    <button class="navbar-toggler" data-bs-toggle="collapse" data-bs-target="#nav">
      <span class="navbar-toggler-icon"></span>
    </button>

    <div id="nav" class="collapse navbar-collapse">
      <ul class="navbar-nav ms-auto">
        <li class="nav-item"><a class="nav-link">Home</a></li>
      </ul>
    </div>
  </div>
</nav>
```

## 📁 Dropdown
```html
<div class="dropdown">
  <button class="btn btn-secondary dropdown-toggle" data-bs-toggle="dropdown">
    Menu
  </button>
  <ul class="dropdown-menu">
    <li><a class="dropdown-item">Item</a></li>
  </ul>
</div>
```

## 📝 Forms
```html
<input class="form-control" placeholder="Name">
<select class="form-select">
  <option>A</option>
</select>
```

## 🔄 Form Groups
```html
<div class="mb-3">
  <label class="form-label">Email</label>
  <input type="email" class="form-control">
</div>
```

## 🪟 Modal
```html
<button class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#m">
  Open
</button>

<div class="modal fade" id="m">
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header"><h5>Title</h5></div>
      <div class="modal-body">Content here</div>
      <div class="modal-footer">
        <button class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
      </div>
    </div>
  </div>
</div>
```

## 🌀 Spinner
```html
<div class="spinner-border text-primary"></div>
```

## 📊 Progress Bar
```html
<div class="progress">
  <div class="progress-bar" style="width: 60%;"></div>
</div>
```

## 🧼 Alerts
```html
<div class="alert alert-warning">Warning!</div>
```

## 🧽 Badges
```html
<span class="badge bg-info">New</span>
```

## 🌐 Toast
```html
<div class="toast show">
  <div class="toast-body">
    Hello!
  </div>
</div>
```

---

# 🌟 Icons
Bootstrap itself does **not** include icons.  
Use Bootstrap Icons:

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.css">
<i class="bi bi-alarm"></i>
```

---

# ⚡ Quick Layout Tips
```html
<div class="container py-5">
  <div class="row g-4">
    <div class="col-md-6">
      <div class="p-4 bg-light rounded shadow">Box</div>
    </div>
  </div>
</div>
```

---
