# Composition & Embedding

- Golang does not support traditional OOP principles.
- It supports compostion through embedding.
- The purpose of embedding is to show a relationship.
- However the embedded classes are independent of each other.

> Note: It is recommended to use `interfaces` if you want to show common behaviour.

## When To Use Embedding

- Combining functionality.
- Get a base behaviour into a custom type.

## Sample Program

```go
package main

import "fmt"


type animal struct {
    name string
    origin string
}

type bird struct {
    animal
    canFly bool
    speed float32
}


func main() {
sparrow := bird{
       animal: animal{name: "Sparrow", origin: "Mountains"},
       canFly: true,
       speed: 250,
    }
}
```
