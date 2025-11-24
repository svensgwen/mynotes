# 🐘 PHP Cheat Sheet — Modern Essentials (2025)

![PHP](../../Images/php.webp)

## 🚀 Basic Syntax
```php
<?php
echo "Hello World!";
?>
```

## 🧩 Variables
```php
$name = "Shashank";
$age = 20;
$price = 9.99;
$isAdmin = true;
```

## 🔢 Data Types
- string  
- int  
- float  
- bool  
- array  
- object  
- null  

## 🎯 Constants
```php
define("APP_NAME", "MyApp");
const PI = 3.14;
```

## 🧮 Operators
```php
+, -, *, /, %
==, ===, !=, !==
&&, ||, !
```

## 🧱 Arrays
```php
$arr = [1, 2, 3];
$map = ["name" => "Bob", "age" => 25];

echo $arr[0];
echo $map["name"];
```

## 🔁 Loops
```php
for ($i = 0; $i < 5; $i++) {}
foreach ($arr as $x) {}
while ($x < 5) { $x++; }
do { $x--; } while ($x > 0);
```

## 🧩 Conditionals
```php
if ($age > 18) {
} elseif ($age == 18) {
} else {
}
```

## 🧱 Functions
```php
function add($a, $b) {
  return $a + $b;
}

$sum = add(2, 3);
```

## 🎒 Default Params
```php
function greet($name = "User") {
  echo "Hi $name";
}
```

## 🛠 Superglobals
```php
$_GET
$_POST
$_SERVER
$_SESSION
$_COOKIE
$_FILES
```

## 🧁 Strings
```php
echo strlen("hello");
echo strtoupper("hi");
echo strtolower("HI");
echo str_replace("hi", "yo", "hi world");
```

## 🧱 Include / Require
```php
include "header.php";
require "config.php";
```

## 🧰 OOP Basics
```php
class User {
  public $name;

  function __construct($n) {
    $this->name = $n;
  }

  function greet() {
    echo "Hi I'm $this->name";
  }
}

$u = new User("Alice");
$u->greet();
```

## 🔗 Inheritance
```php
class Animal {
  function sound() { echo "noise"; }
}
class Dog extends Animal {
  function sound() { echo "woof"; }
}
```

## 🧱 Interfaces
```php
interface Shape {
  public function area();
}
```

## 🧨 Error Handling
```php
try {
  throw new Exception("Error!");
} catch (Exception $e) {
  echo $e->getMessage();
}
```

## 🗃️ Sessions
```php
session_start();
$_SESSION["user"] = "Shashank";
echo $_SESSION["user"];
```

## 🍪 Cookies
```php
setcookie("token", "abc123", time()+3600);
echo $_COOKIE["token"];
```

## 🗂️ File Handling
```php
file_put_contents("a.txt", "hello");
$content = file_get_contents("a.txt");
```

## 🔌 PDO (Database)
```php
$db = new PDO("mysql:host=localhost;dbname=test", "user", "pass");

$stmt = $db->prepare("SELECT * FROM users WHERE id=?");
$stmt->execute([1]);
$data = $stmt->fetch(PDO::FETCH_ASSOC);
```

## 🌐 Simple API Call
```php
$response = file_get_contents("https://api.example.com");
$data = json_decode($response, true);
```

## 🧼 Composer
```bash
composer init
composer require package/name
composer update
```

