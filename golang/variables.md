# Variables in GO

Main types of variables:
- string
- bool 
- int int8 int16 int32 int64
- uint uint8 uint32 uint64 uintptr
- byte - alias for uint8
- rune - alias for int32
- float32 float64
- complex64 complex128


# How to Create Variables

## Using `var` Keyword

```go
var name string = "DaveSaah"
```

- Value type is inferred from the value.
    - It is not necessary to explicitly state it.
    - Only make explicitly typed variable definitions when they are not the default types.

## Using `const` Keyword

```go
const pi = 3.14
```

- Observation: Defining a const variable without using it does not throw an er    ror.

## Shorthand Method

```go
name := "DaveSaah"
```

- It can only be used within a function.


## Checking Value Type

```go
fmt.Printf("%T\n", age)
```

- `%T` is a verb that gets the type of a value.

# Note

- Every variable in Go must be used, else an error is raised.

> search and make notes about fmt pkg -> https://golang.org/pkg/fmt

- Multiple assignments is possible.

```go
const food, color = "Matoke", "Blue"
```
- The same variable cannot be declared more than once in the same scope.

> Shadowing occurs when a variable takes the declaration defined in its inner scope. For example if a variable is declared at the package level and in a function's scope, the value the variable keeps is the one declared in the innermost scope (which is the function level).


# Multiple Declarations

- Multiple variables can be declared in go using a `var` block.

```go
var (
    name = "DaveSaah"
    age = 20
    fruit = "Orange"
)
```

- `var` blocks can be used to declare related variables together.

