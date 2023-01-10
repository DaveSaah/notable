# If Statements

## Syntax

```ga
// if
if boolean_expression {
    // code
}

// if-else
if boolean_expression {
    // code
} else {
    // code
}

// if-else if-else
if boolean_expression {
    // code
} else if boolean_expression {
    // code
} else {
    // code
}
```

## Initialiser Syntax

```go
// Sample
populations := map[string]int {
    "Ghana": 23,
    "Uganda": 33,
    "Senegal": 55,
}

if pop, ok := populations["Ghana"]; ok {
    fmt.Println(pop)
}
```
- The initialiser is separated from the boolean expression by a semi-colon (`;`).
- `pop` is set to the value of the population of Ghana.
- `ok` stores `true` or `false` depending on the existence of a key in `populations`.
- In the `if` statement above, it prints the population of Ghana if "Ghana" exists as a key in `populations`.

## Comparison Operators

| Operator | Symbol |
| --- | --- |
| less than | `<` |
| greater than | `>` |
| less than or equal to | `<=` |
| greater than or equal to | `>=` |
| not equal | `!=` |
| equality | `==` |

## Logical Operator

| Operator | Symbol |
| --- | --- |
| or | `||` |
| and | `&&` |
| not | `!` |

## Short Circuiting

- In a compound boolean expression, Go short circuits its evaluation if the outcome cannot be changed if the subsequent code is run.
- E.g. In a compound boolean expression with `or`, if one expression evaluates to `true`, the compiler short circuits the operation.
- In the same vein, in a compound boolean expression with `and`, if one expression evaluates to `false`, the compiler short circuits the operation.

# Switch Statements

It is special-purpose if-statement where there are many if-else's involved.

## SYNTAX

```go
// Simple
switch tag {
    case val1:
        // code
    case val2:
        // code
    default:
        // code
}

// multiple test values
switch tag {
    case val1, val2:
        // code
    case val3, val4, val5:
        // code
    default:
        // code
}

// initialiser syntax
switch tag := expression; tag {
    // code
}

// test cases as boolean expression; tagless syntax
switch {
    case boolean_expression:
        // code
    ...
}
```

## Fallthrough

- The `fallthrough` keyword is used when you want to run the test case after the valid one has passed.
- `fallthrough` is logicless. This means that if the next test case is false, the code block still execute.

```go
// example
switch {
    case 5 <= 10:
        fmt.Println("Less than 10")
        fallthrough
    case 5 <= 20:
        fmt.Println("Less than 20")
}
```
## Type Switches

- It is used to check the type of a value.
- The type `interface` can take any data type available in Go as a value.

```go
// sample
var i interface{} = 1

switch i.(type) {
    case int:
        fmt.Println("integer")
    case float64:
        fmt.Println("float 64bit")
    case string:
        fmt.Println("string")
    default:
        fmt.Println("This is another type")
}
```

## Notes

- A `tag` is value that is tested by cases in a `switch` statement.
- A `break` keyword is implied in switch statements in `Go`.
- Array types are very different from any other arrays. They have to have the same data type and size for them to be considered equal.
- `break` keyword can be used to exit the execution of a case block early. This is useful if you're running a logical test within the block.
- The delimiter for switch statement blocks are the keywords: `case` and `default`.
