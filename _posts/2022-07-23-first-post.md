---
title: First Post
tags:
 - Test
 - Random
comments: true
---

This is the first post of this blog.

<!--more-->
### Introduction

So I created blog using GitHub Pages. My plan is to use this blog as a place to write about topics that I studied/learned about, and other random stuff.
Most of the time I'll probably post stuff related to computer science and math, but I can't be sure.

Here are a few things I want to mention:
* I wasn't able to enable comments, but I am trying.
* English is not my native language, and there could be multiple grammatical errors. Please ignore for the tume being.

Currently I don't have anything interesting to post about, but at the same time want to write something, so I'll just show Hello World written in multiple differnt languages, in no particular order(I'll keep adding more if I fell like it).

### C
```c
#include <stdio.h>

int main(){
  printf("Hello World");
  return 0;
}
```

### C++
```cpp
#include <iostream>

int main(){
  std::cout << "Hello World";
  return 0;
}
```

### C#
```csharp
namespace HelloWorld
{
  class HW{
    static void Main(string[] args){
      System.console.WriteLine("Hello World");
    }
  }
}
```

### Python
```python
print("Hello World")
```

### Java
```java
class HelloWorld{
  public static void main(String[] args){
    System.out.println("Hello World");
  }
}
```

### JavaScript
```javascript
console.log("Hello World");
```

### Pascal
```pascal
program Hello;
begin
  writeln('Hello World');
  readln;
end.
```

### Ruby
```ruby
puts 'Hello World'
```

### Kotlin
```kotlin
fun main(args: Array<String>){
  println("Hello World");
}
```

### Swift
```swift
println("Hello World");
```

### Node.js
```javascript
var http = require('http');

http.createServer(function (req,res){
  res.writeHead(200, {'Content-Type': 'text/html'});
  res.end('Hello World');
}).listen(8080);
```

### Text
```
Hello World
```

### Go
```go
package main

import "fmt"

func main(){
  fmt.Println("Hello World")
}
```

### D
```d
import std.stdio;

void main(){
  writeln("Hello World");
}
```
