# ⚔️ C++ Cheat Sheet

![CPP](../../Images/cpp.webp)

## 🚀 Basic Structure
```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Hello World\n";
    return 0;
}
```

## 🧮 Variables & Types
```cpp
int a = 10;
float b = 3.14f;
double c = 2.718;
char d = 'x';
bool e = true;
string s = "hello";
auto x = 42;     // type inference
```

## 📦 Input / Output
```cpp
int x;
cin >> x;
cout << "Value: " << x << endl;
```

## ✨ Strings
```cpp
string s = "hello";
s.size();
s += " world";
s.substr(0, 3);
```

## 🔁 Loops
```cpp
for (int i=0; i<5; i++) {}
while (condition) {}
do {} while (condition);
```

## 🌿 If / Else
```cpp
if (x > 0) {} 
else if (x == 0) {} 
else {}
```

## 🧱 Arrays & Vectors
```cpp
int a[3] = {1,2,3};

vector<int> v = {1,2,3};
v.push_back(4);
v.size();
v[0];
for (int n : v) {}
```

## 🧩 Functions
```cpp
int add(int a, int b) {
    return a + b;
}

auto multiply(int x, int y) -> int {
    return x * y;
}
```

## 🫙 References & Pointers
```cpp
int x = 10;
int& ref = x;   // reference
int* p = &x;    // pointer
*p = 20;
```

## 🔨 Classes
```cpp
class Person {
public:
    string name;
    int age;

    Person(string n, int a) : name(n), age(a) {}
    void greet() { cout << "Hi " << name; }
};
```

## 🧬 Inheritance
```cpp
class Animal { public: void speak() {} };
class Dog : public Animal { public: void bark() {} };
```

## 🧰 Constructors / Destructors
```cpp
class A {
public:
    A() { cout << "init"; }
    ~A() { cout << "destroy"; }
};
```

## 🧱 Encapsulation
```cpp
class Box {
private:
    int value;
public:
    void set(int v) { value = v; }
    int get() const { return value; }
};
```

## 🧵 Const Correctness
```cpp
void foo(const int x);
void bar() const;       // method won’t modify object
```

## 🧮 Operator Overloading
```cpp
class Vec {
public:
    int x;
    Vec(int x) : x(x) {}
    Vec operator+(const Vec& other) {
        return Vec(x + other.x);
    }
};
```

## 🔧 Templates
```cpp
template<typename T>
T add(T a, T b) {
    return a + b;
}
```

## 📚 Standard Library (STL)
### — Containers:
```cpp
vector<int>
array<int,5>
set<int>
map<string,int>
unordered_map<string,int>
```

### — Useful Algorithms:
```cpp
sort(v.begin(), v.end());
reverse(v.begin(), v.end());
find(v.begin(), v.end(), 3);
```

## 🛡️ Smart Pointers
```cpp
unique_ptr<int> p1 = make_unique<int>(10);
shared_ptr<int> p2 = make_shared<int>(20);
weak_ptr<int> w = p2;
```

## 🧵 C++20 Goodies
```cpp
auto f = [] (int x) { return x * 2; };  // lambdas
ranges::sort(v);                       // C++20 ranges
```

## 💥 Error Handling
```cpp
try {
    throw runtime_error("error");
} catch (exception& e) {
    cout << e.what();
}
```

## 🧪 File I/O
```cpp
#include <fstream>

ofstream out("file.txt");
out << "hello";

ifstream in("file.txt");
string line;
getline(in, line);
```

## ⚡ Compile & Run
```bash
g++ main.cpp -std=c++20 -O2 && ./a.out
```
