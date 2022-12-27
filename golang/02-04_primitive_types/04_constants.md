# Naming Conventions

- Constant declarations are preceeded by the `const` keyword.

```go
const myConst = 23
```

# Characteristics of Constants

- They are immutable.
- They have to be assigned at compile time. Any code that needs to be executed to get the value of a constant will throw an error.

```go
const myConst = math.Sin(1.57)  // this throws an error
const myConst = 23  // this is acceptable
```

> Constants cannot to be set to a value that will be determined at runtime.


# Enumerated Constants

```go
const myConst = iota

func main() {
    fmt.Printf("%v, %T\n", myConst, myConst)
}
```

- `iota` is a counter that can be used when creating an enumerated constant.
- `iota` is scoped to a `const` block.

# Enumerated Expressions

- Constants can also be declared in `const` block just like variables.

```go
const (
    a = iota
    b = iota
)

const (
    a1 = iota
    b1
    c1
    d1
)
```


