# Loops

- In Go, only the `for` statement is used when defining loops.

## Simple Loops

```go
// SYNTAX

for initialiser; condition; expression_executed_after_each_run (mostly the increament operation) {
    // code
}

// example

for i := 0; i <= 5; i++ {
    fmt.Println(i)
}

// To use an already defined variable in a loop
i := 0

for ; i < 5; i++ {
    fmt.Println(i)
}

// Placing the increamenter in the loop
for i := 0; i < 5; {
    // code
    i++
}
```

## While Loop Implementation

```go
// SYNTAX

for boolean_expression {
    // code
}

// example
i := 0

for x < 5 {
    fmt.Println(i)
    i++
}
```

## Do-while Loop Implementation

```go
// SYNTAX
for {
    // code
}
```

## Labelling

- When using nested loops, the `break` statement breaks the inner loop while the outer loop is left to run.
- To deal with such situations, we can use labels in our code.

```go
func main() {
    Loop:
	    for i := 1; i <= 3; i++ {
	        for j := 1; j <= 3; j++ {
		        val := i * j
		        fmt.Println(val)
		        if val >= 3 {
		            break Loop
		        }
	        }
	    }
}
```

## Working With Collections

```go
// for-range loop

// SYNTAX
for key, value := range collection_datatype {
    // code
}
```

- `for` loop stops when the items in the collection is finished.
- If you want only the keys from `range`, just assign a variable to it. E.g. `keys := range []int{1, 2, 3}`.
- If you only want the values, you can use the null variable, `_` (underscore). E.g. `_, values := []int{1, 2, 3}`.
- Examples of data types we can range in Go:
    - maps
    - lists
    - slices
    - strings
    - channels

# Note

- The increament/decreament operation is a statement, not an expression.

```go
j = j++     // results in an error
```

- Go has `continue` keyword.
- Go has nested loops.
- The `break` statement breaks out of a loop while a `continue` statement break out of the currrent iteration of a loop without exiting the main loop.
