# Defer (Defer Functions)

- Used to delay execution of a statement until function exits.

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
- Defer statement doesn't take a function itself, but a function call.

# Panic

- Makes your go program enter a state where it can no longer continue to run.
- Go does not have exceptions; it makes use of panic.
- In Go, we return error values; we don't throw exceptions.
- Situations that make Go applications unable to continue is considered exceptional.
- These situations are handled using `panic`.
- Go runtime automatically generates a panic whenever there is an exception.

```go
// Example

a, b := 1, 0
ans := a / b
fmt.Println(ans)
```

## Manually Generating Panic

```go
// SYNTAX
panic(msg)
```

- The program stops after a `panic`.
- Panics happen after `defer` statements are executed.

> ## Execution Priority 
>
> 1. Main function
> 2. Defer statements
> 3. Panic statements
> 4. Handle return value

### Advantages of Execution Priority

- Defer statements that are going to close resources are going to succeed even if the application panics.

# Recover

- Allows you to save the state of your application after a `panic`.
- Manages the behaviour of a panicking goroutine.
- It stops a panicking sequence by restoring normal execution and retrieves the error value passed to the call of panic.

> - `recover()` function is normally called inside a deferred function because when a function panics, it stops executing. Since deferred statements are run after a function has stopped, it is safe to place the `recover` function in a `defer` function.
> - If `recover` is called outside a deferred function, it will not stop a panicking sequence.

- The function that recovers stops executing. However, functions higher up the call stack (i.e the function that called the function that panicked and recovered) will continue to run.
