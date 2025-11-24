# 🚀 Vite + React Project

![ReactJs](../../Images/reactjs.webp)

This guide shows how to create a **React + Vite** app using **Yarn** and add **Bootstrap** for styling.

---

## ⚡ Step 1: Create a New React App with Vite

Run this command to create a new project:

```bash
yarn create vite my-app-name --template react
```

Or, if you prefer **TypeScript**:

```bash
yarn create vite my-app-name --template react-ts
```

Then move into your project folder:

```bash
cd my-app-name
```

Install dependencies:

```bash
yarn
```

Run the dev server:

```bash
yarn dev
```

Or run the app:

```bash
yarn vite
```

## Congratulations our app will now be live on Localhost

[localhost:5173](http://localhost:5173/) 🎉

---

## 🎨 Step 2: Install React Bootstrap

If you want to use **Bootstrap components as React components**, install React-Bootstrap:

```bash
yarn add react-bootstrap
```

Example usage:

```jsx
import Button from 'react-bootstrap/Button';

function App() {
  return <Button variant="primary">Click Me</Button>;
}

export default App;
```

NOTE: React-Bootstrap manages JS behavior automatically.

---

## ✨ Step 3: Clean your App (app.jsx, app.css)

Delete all text in "**app.css**"

Example component (**app.jsx**):

```jsx
function App() {
  return (
    <div style={{ fontFamily: "sans-serif", padding: "2rem" }}>
      <h1>hello world</h1>
      <p>the future’s loading…</p>
    </div>
  );
}

export default App;
```


---

## ✅ Summary

| Step | Action | Command |
|------|---------|----------|
| 1 | Create Vite + React app | `yarn create vite my-app --template react` |
| 2 | Install dependencies | `yarn` |
| 3 | Run dev server | `yarn dev` |
| 4 |  Add React-Bootstrap | `yarn add react-bootstrap` |

---

Now your **Vite + React** setup is fully powered by **Bootstrap’s** sleek design system and ready to build something beautiful. 💥

## 🖼️ Adding Images in a Vite + React Project

This guide shows the best ways to include and use images in your **Vite + React** app.

---

## 📁 Step 1: Add Your Image to the Project

Put your image inside the `src/assets/` folder.  
Example structure:

```txt
my-app/
├─ src/
│  ├─ assets/
│  │  └─ logo.png
│  ├─ App.jsx
│  └─ main.jsx
```

---

## 🧠 Step 2: Import and Use the Image in React

In `App.jsx`, import your image and use it inside JSX:

```jsx
import React from 'react';
import logo from './assets/logo.png';

function App() {
  return (
    <div className="container text-center mt-5">
      <h1 className="text-primary mb-3">Hello World</h1>
      <img src={logo} alt="Logo" width="200" />
    </div>
  );
}

export default App;
```

✅ **Why this is best:**  
Vite optimizes images during build — handles hashing, caching, and asset management automatically.

---

## 🌐 Step 3 (Alternative): Use Public Folder for Static Images

If you have assets that won’t change (like favicons, brand images, etc.), put them in the `public/` folder:

```txt
my-app/
├─ public/
│  └─ banner.jpg
├─ src/
│  └─ App.jsx
```

Then reference them **without import**:

```jsx
function App() {
  return (
    <div className="text-center mt-5">
      <img src="/banner.jpg" alt="Banner" width="400" />
    </div>
  );
}

export default App;
```

✅ **Why this works:**  
Files in `public/` are served as-is from the root. Perfect for static assets or images loaded by URL.

---

## ⚡ Step 4: Add Some Bootstrap Styling (Optional)

If you’re using Bootstrap, you can style your images easily:

```jsx
<img src={logo} alt="Logo" className="img-fluid rounded shadow" />
```

---

## ✅ Summary Image

| Method | When to Use | Example |
|--------|--------------|----------|
| Import from `src/assets` | When the image is part of your app build | `import logo from './assets/logo.png'` |
| Use from `public/` | When the image is static or externally referenced | `<img src="/banner.jpg" alt="..." />` |

---

Now your React app handles images the **modern, Vite-optimized** way — clean, fast, and production-ready. 💥

## Create new Component

```jsx
function MyComponent() {
  return (
    <div>
      <h1>Hello from my component</h1>
    </div>
  );
}

export default MyComponent;
```

## Select Options in React

### Step 1: Install the package

```bash
yarn add react-select
```

### Step 2: Use it in your component

```jsx
import Select from "react-select";

function MultiSelect() {
  const options = [
    { value: "react", label: "React" },
    { value: "vue", label: "Vue" },
    { value: "svelte", label: "Svelte" },
    { value: "angular", label: "Angular" }
  ];

  return (
    <Select
      options={options}
      isMulti
      placeholder="Pick your language..."
    />
  );
}

export default MultiSelect;
```

### Step 3: Optional (Get the Value)

```jsx
<Select
  options={options}
  isMulti
  onChange={(selected) => {
    console.log(selected);
  }}
/>
```

### Step 4: Optional (Preselect Values)

```jsx
<Select
  options={options}
  isMulti
  defaultValue={[options[0], options[2]]}
/>
```
