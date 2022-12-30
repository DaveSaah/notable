# Anonymous Structs

## Characteristics of Anonymous Structs

- Both the struct definition and initialisation is done simultaneously.
- They cannot be used anywhere else.
    - They do not have an independent name that can be referred to in a program.

> **Struct Definition** defines the structure of a struct.
> **The initialiser** defines the data that would be put into a struct.

## When To Use Anonymous Structs

- When the lifetime of a struct is small.
- When a struct is going to be used only once in the program.

> You do not need to make that struct available for the entire package in your application.

## Creating Anonymous Structs

```go
// SYNTAX
var variable = struct{definition}{initialisers}

// example
var doctor = struct{name string}{name: "John Darwin"}
```
