# Anonymous Functions

## SYNTAX

```go
func(param data-type) {
    // some code here
}(param)
```

- They are defined and executed at the same time.
- `params` are defined if you want to access variables from an outside scope.

- Anonymous functions can be declared as variables. `()` is omitted in its definition.

```go
f := func() {
    fmt.Println("Hello")
}

f()
```

- The default type signature is `func()`.
- If the anonymous function has a parameter and return type, the type signature changes to: `func(params data-type) return-type`
