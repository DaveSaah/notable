# Defer (Defer Functions)

> Allows you to invoke a function, but delay its execution to some future point in time.

```go
// using defer
defer fmt.Println("Hello")
```

- It executes any function that are passed into it after the function finishes its final statement, but before it returns.
- The `defer` keyword executes in LIFO (Last In First Out) when multiple statements are made.

```go
// Example

defer fmt.Println("Hello")
defer fmt.Println("World")
defer fmt.Println("Some")
```
- Allows you to associate the opening of a resource and the closing of the resource next to each other.
- A `defer` statement accesses the value of a variable at the time it is called, not when the statement is executed.

# Panic

> Makes your go program enter a state where it can no longer continue to run.

- 

# Recover

> Allows you to save the state of your application after a `panic`.
