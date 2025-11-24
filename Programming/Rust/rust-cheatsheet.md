# 🦀 Rust Cheat Sheet
![Rust](../../Images/rust.webp)

## 🚀 Basics
```rust
fn main() {
    println!("Hello, Rust!");
}
```

## 📦 Variables
```rust
let x = 10;          // immutable
let mut y = 20;      // mutable
const PI: f64 = 3.14;
```

## 🔢 Data Types
```rust
i32, i64, u32, usize
f32, f64
bool
char
&str
String
```

## 🎯 Strings
```rust
let s = String::from("hello");
s.push('!');
s.push_str(" world");

let slice: &str = &s[0..5];
```

## 🧱 Tuples & Arrays
```rust
let t = (1, "hi", 3.14);
let arr = [1, 2, 3];
let mut vec = vec![1, 2, 3];
vec.push(4);
```

## 🔁 Loops
```rust
for i in 0..5 {}
while x < 5 {}
loop { break; }
```

## 🧩 Conditionals
```rust
if x > 5 {
} else if x == 5 {
} else {
}
```

## ⚡ Match
```rust
match num {
    1 => println!("one"),
    2 | 3 => println!("two or three"),
    _ => println!("other"),
}
```

## 👉 Ownership Rules
- One owner at a time  
- Move semantics by default  
- Borrowing with `&` and `&mut`

```rust
let s1 = String::from("hi");
let s2 = s1;            // move
// println!("{}", s1);  // error

let s3 = s2.clone();    // deep copy
```

## 🪢 Borrowing
```rust
fn print_len(s: &String) {
    println!("{}", s.len());
}

fn modify(s: &mut String) {
    s.push('x');
}
```

## 🎁 Functions
```rust
fn add(a: i32, b: i32) -> i32 {
    a + b
}
```

## 🧱 Structs
```rust
struct User {
    name: String,
    age: u32,
}

let u = User {
    name: "Bob".into(),
    age: 20,
};
```

## 🧩 Impl (Methods)
```rust
impl User {
    fn greet(&self) {
        println!("Hi {}", self.name);
    }
}
```

## 🧬 Enums
```rust
enum Status {
    Ok,
    Err(String),
}

let s = Status::Err("oops".into());
```

## 🔥 Option / Result
```rust
let x: Option<i32> = Some(10);
let y = None;

let res: Result<i32, String> = Ok(10);

match res {
    Ok(v) => println!("{}", v),
    Err(e) => println!("err: {}", e),
}
```

## 🧵 Pattern Matching
```rust
let (a, b) = (10, 20);

if let Some(v) = x {
    println!("{}", v);
}

while let Some(v) = vec.pop() {}
```

## 📦 Vectors
```rust
let mut v = Vec::new();
v.push(1);
v.push(2);

for n in &v {}
for n in &mut v {}
```

## 🔗 Traits
```rust
trait Greet {
    fn hello(&self);
}

struct Person;

impl Greet for Person {
    fn hello(&self) {
        println!("yo");
    }
}
```

## 🌱 Generics
```rust
fn add<T: std::ops::Add<Output = T>>(a: T, b: T) -> T {
    a + b
}
```

## 🧨 Error Handling
```rust
fn risky() -> Result<(), String> {
    Err("nope".into())
}

fn main() {
    if let Err(e) = risky() {
        println!("Error: {}", e);
    }
}
```

## ⚙️ Modules
```rust
mod utils {
    pub fn hi() {
        println!("hi");
    }
}

utils::hi();
```

## 🛠️ Cargo Commands
```bash
cargo new app
cargo run
cargo build --release
cargo check
cargo fmt
cargo add crate_name
cargo test
```

## 🧪 Unit Tests
```rust
#[cfg(test)]
mod tests {
    #[test]
    fn it_works() {
        assert_eq!(2 + 2, 4);
    }
}
```

## 🧵 Async / Await
```rust
use tokio::time::{sleep, Duration};

#[tokio::main]
async fn main() {
    sleep(Duration::from_secs(1)).await;
}
```

## 🌐 HTTP (Reqwest)
```rust
let body = reqwest::get("https://api.example.com")
    .await?
    .text()
    .await?;
```

