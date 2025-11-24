# 🐉 Lua Cheat Sheet — Essentials

![alt text](lua.webp)

## ✨ Variables
```lua
x = 10
local y = 20   -- local scope
name = "Shashank"
```

## 🔢 Data Types
```lua
num = 42
str = "hello"
bool = true
tbl = {1, 2, 3}
```

## 🔁 Loops
```lua
for i = 1, 5 do
  print(i)
end

while x < 10 do
  x = x + 1
end

repeat
  x = x - 1
until x == 0
```

## 🧩 Conditionals
```lua
if x > 5 then
  print("big")
elseif x == 5 then
  print("equal")
else
  print("small")
end
```

## 🧱 Tables (Arrays + Maps)
```lua
arr = {10, 20, 30}       -- array
user = {name="Bob", age=20}  -- dict-style

print(arr[1])
print(user.name)
```

## 🎯 Functions
```lua
function add(a, b)
  return a + b
end

sub = function(a, b)
  return a - b
end
```

## 🌀 Pairs / IPairs
```lua
for i, v in ipairs(arr) do
  print(i, v)
end

for k, v in pairs(user) do
  print(k, v)
end
```

## 📦 Modules (require)
```lua
local mathlib = require("mathlib")
```

## 🧨 Metatables (Basics)
```lua
mt = {
  __add = function(a, b)
    return a.value + b.value
  end
}

obj1 = {value = 10}
obj2 = {value = 20}
setmetatable(obj1, mt)
setmetatable(obj2, mt)

print(obj1 + obj2)  -- 30
```

## 🧱 OOP (Classic Lua Style)
```lua
Person = {}
Person.__index = Person

function Person:new(name)
  return setmetatable({name = name}, self)
end

function Person:greet()
  print("Hi, I'm " .. self.name)
end

p = Person:new("Alice")
p:greet()
```

## 🗂️ File I/O
```lua
file = io.open("test.txt", "w")
file:write("hello")
file:close()
```

## 🧯 Error Handling
```lua
status, err = pcall(function() error("oops") end)
print(status, err)
```
