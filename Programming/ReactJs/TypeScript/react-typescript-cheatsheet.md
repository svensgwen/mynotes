# ⚛️ React + 🟦 TypeScript Cheat Sheet

![React Typescript](../../../Images/react-typescript.webp)

---

No fluff. Just the real path.

---
⚡ CREATE PROJECT (VITE)

---
```bash
npm create vite@latest my-app -- --template react-ts
cd my-app
npm install
npm run dev
```

Open the URL shown in terminal.
Your app is breathing now.

---
🧼 CLEAN THE BOILERPLATE
---

Delete the noise:
```bash
rm src/assets/react.svg
rm src/App.css
rm src/index.css
```
---

🧠 SIMPLIFY main.tsx
---
Edit src/main.tsx:
```tsx
import React from 'react'
import ReactDOM from 'react-dom/client'
import App from './App'

ReactDOM.createRoot(document.getElementById('root')!).render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
)
```

---
✨ RESET App.tsx
---

Edit src/App.tsx:
```tsx
const App = () => {
  return <h1>⚛️ Fresh project. Clean slate.</h1>
}

export default App
```

---
🧠 POWER-UPS (OPTIONAL BUT GOATED)
---

---
🎯 ABSOLUTE IMPORTS
---
Edit tsconfig.json:
```json
{
  "compilerOptions": {
    "baseUrl": "src"
  }
}
```
Now import clean:

```jsx
import Button from 'components/Button'
```

──────────────────────────────
🧹 PRETTIER (CODE WITH DRIP)
──────────────────────────────

npm i -D prettier

Create .prettierrc:

{
  "semi": false,
  "singleQuote": true
}

──────────────────────────────
🔍 ESLINT (BUG HUNTER MODE)
──────────────────────────────

npm i -D eslint
npx eslint --init

──────────────────────────────
☠️ AVOID
──────────────────────────────

❌ CRA
❌ bloated starters
❌ copy-paste boilerplate with no clue

──────────────────────────────
🎤 FINAL WORD
──────────────────────────────

No magic.
No mess.
No excuses.

Just React.
Just TypeScript.
Just you.

Go build something unreal. ⚡



## 📦 Basic Component (FC)

```tsx
type Props = {
  title: string
  count?: number
}

const MyComponent: React.FC<Props> = ({ title, count = 0 }) => {
  return <h1>{title} — {count}</h1>
}
```

---

## 🎯 Typing Props Inline

```tsx
const Button = ({ label, onClick }: { label: string; onClick: () => void }) => (
  <button onClick={onClick}>{label}</button>
)
```

---

## 🧩 useState Hook

```tsx
const [value, setValue] = useState<string>("hello")
const [num, setNum] = useState<number>(0)
const [obj, setObj] = useState<{ x: number }>({ x: 10 })
```

---

## 🔄 useEffect Hook

```tsx
useEffect(() => {
  console.log("mounted")

  return () => console.log("cleanup")
}, []) // 👈 deps
```

---

## ⚙️ useRef

```tsx
const inputRef = useRef<HTMLInputElement>(null)

useEffect(() => {
  inputRef.current?.focus()
}, [])
```

---

## 🧪 Event Types

```tsx
const handleChange = (e: React.ChangeEvent<HTMLInputElement>) => {
  console.log(e.target.value)
}

const handleSubmit = (e: React.FormEvent<HTMLFormElement>) => {
  e.preventDefault()
}
```

---

## 🚀 Async Functions

```tsx
const fetchData = async (): Promise<User[]> => {
  const res = await fetch("/api/users")
  return res.json()
}
```

---

## 🌲 Typing Children

```tsx
type Props = {
  children: React.ReactNode
}
```

---

## 🏗️ Custom Hooks

```tsx
const useToggle = (initial = false) => {
  const [state, setState] = useState<boolean>(initial)
  const toggle = () => setState(s => !s)
  return { state, toggle }
}
```

---

## 🧱 Typing Context

```tsx
type Theme = "light" | "dark"

const ThemeContext = createContext<Theme>("light")

const useTheme = () => useContext(ThemeContext)
```

---

## 🔌 Typing API Data

```tsx
interface User {
  id: number
  name: string
  email: string
}
```

---

## 🧵 Union & Literal Types

```tsx
type Status = "idle" | "loading" | "error"
```

---

## 🏗️ Component with Generics

```tsx
function Wrapper<T>({ item }: { item: T }) {
  return <div>{JSON.stringify(item)}</div>
}
```

---

## 🧰 Utility Types

```tsx
type PartialUser = Partial<User>
type UserPreview = Pick<User, "id" | "name">
type UserWithoutEmail = Omit<User, "email">
```

---

## 🎛️ Styled Components Example

```tsx
import styled from "styled-components"

const Box = styled.div<{ bg: string }>`
  padding: 1rem;
  background: ${({ bg }) => bg};
`
```

---

## 🔋 Default Props (with TS)

```tsx
type Props = {
  size?: number
}

const Avatar = ({ size = 24 }: Props) => <img style={{ width: size }} />
```

---

## 🌐 React Router (TS)

```tsx
<Route path="/user/:id" element={<UserPage />} />

const { id } = useParams<{ id: string }>()
```

---

## 🧱 Redux Toolkit (TS)

```tsx
interface CounterState {
  value: number
}

const initialState: CounterState = { value: 0 }
```

---

## 🧪 Testing (React Testing Library)

```tsx
render(<MyComponent title="Hello" />)
expect(screen.getByText("Hello")).toBeInTheDocument()
```

---

## 📚 Tips

- Always prefer **interfaces** for objects.
- Use **type** for unions & complex utilities.
- Store reusable types in `types/` folder.
- Enable strict mode in TS for max safety.

---

## 🌟 You’re set — build boldly, code freely.  
