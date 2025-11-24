# 🐹 Go (Golang) Cheat Sheet — Modern Essentials

![GOlang](../../Images/go.webp)

## 🚀 Setup
```bash
go mod init myapp
go run main.go
go build
go fmt ./...
```

## 📦 Basic Program
```go
package main

import "fmt"

func main() {
    fmt.Println("Hello Go!")
}
```

## 🧩 Variables & Types
```go
var x int = 10
y := 20 // shorthand
const pi = 3.14

var (
    a int
    b string
)
```

Primitive types:
```go
int, float64, bool, string, byte, rune
```

## 🎯 Functions
```go
func add(a int, b int) int {
    return a + b
}

func mult(a, b int) (int, int) {
    return a * b, a + b
}
```

## 🔁 Loops
```go
for i := 0; i < 5; i++ {}

for i < 10 {
    i++
}

for { // infinite loop
    break
}
```

## 🧱 Conditionals
```go
if x > 5 {
} else if x == 5 {
} else {
}

switch n {
case 1:
    fmt.Println("one")
case 2, 3:
    fmt.Println("two or three")
default:
    fmt.Println("other")
}
```

## 📦 Arrays & Slices
```go
arr := [3]int{1,2,3}
slice := []int{1,2,3}

slice = append(slice, 4)

sub := slice[1:3]
```

## 🔗 Maps
```go
m := map[string]int{
    "a": 1,
    "b": 2,
}

m["c"] = 3
delete(m, "a")
val, ok := m["b"]
```

## 🧩 Structs
```go
type User struct {
    Name string
    Age  int
}

u := User{"Bob", 25}
u2 := User{Name: "Ana", Age: 22}
```

## 🧲 Methods
```go
func (u User) greet() {
    fmt.Println("Hi, I'm", u.Name)
}

func (u *User) birthday() {
    u.Age++
}
```

## 🧱 Interfaces
```go
type Shape interface {
    Area() float64
}

type Square struct{ Side float64 }

func (s Square) Area() float64 {
    return s.Side * s.Side
}
```

## 🧵 Goroutines (Concurrency)
```go
go func() {
    fmt.Println("Async!")
}()
```

## 📬 Channels
```go
ch := make(chan int)

go func() {
    ch <- 42
}()

x := <-ch
```

Buffered:
```go
ch := make(chan int, 2)
```

## ⏳ Select
```go
select {
case msg := <-ch1:
    fmt.Println(msg)
case <-time.After(1 * time.Second):
    fmt.Println("timeout")
}
```

## 🗂️ Error Handling
```go
func risky() error {
    return errors.New("oops")
}

if err := risky(); err != nil {
    fmt.Println("error:", err)
}
```

## 📄 File I/O
```go
data, err := os.ReadFile("a.txt")
os.WriteFile("b.txt", []byte("hello"), 0644)
```

## 🧰 Useful Packages
```go
import (
    "fmt"
    "os"
    "time"
    "strings"
    "math"
)
```

## 🌍 HTTP Server (Mini)
```go
package main
import (
    "fmt"
    "net/http"
)

func main() {
    http.HandleFunc("/", func(w http.ResponseWriter, r *http.Request) {
        fmt.Fprintln(w, "hello")
    })

    http.ListenAndServe(":8080", nil)
}
```

