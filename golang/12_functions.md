# Functions

## Syntax

```go
func function_name(parameter type) return-type {
    // some code
}

// example
func greet(name string) string {
    return "Hello " + name
}

// if the return-type is void, no return type is entered.
func greet(name string) {
    fmt.Println(name)
}
```

- If the parameters are all of one type, just one type declaration is made.

```go
func getSum(num1, num2, num3, int) int {
    return num1 + num2 + num3
}
```

## Why You Might Need To Pass Pointers As Arguments

If arguments need to be modified by a function to be used outside its scope.

## Variadic Parameters

E.g.

```go
func sum(values ...int) {
        fmt.Println(values)
    }
```

- The Go runtime wraps all the values into a slice.
- There can only be one variadic parameter and it has to be the last one.

The following example is also valid.

```go
func sum(msg string, values ...int) {
    fmt.Println(msg, values)
}
```

## Using Named Return Values

```go
func sun(values ...int) (result int) {
    for _, num := range values {
        result += num
    }
    return
}
```

- It is syntactic sugar for declaring a `result` variable.
- The variable is available in the scope of the `sum` function.
- The value will be implicitly returned when the function ends.

## Multiple Return Values

```go
func main() {
    d, err := divide(5.0, 0.0)
    if err != nil {
        fmt.Println(err)
        return
    }
}

func divide(a, b float64) (float64, error) {
    if b == 0.0 {
        return 0.0, fmt.Errorf("Cannot divide by zero")
    }

    return a / b, nil
}
```
