- There are 3 primitive types:
    - Boolean types.
    - Numeric types.
        - Integers.
        - Floats.
        - Complex numbers.
    - Text types.

- `%v` verb points to the value of a variable in `fmt.Printf`
- An initialised variable always points to a zero value in its corresponding data type.

```go
var isWhat string       // gives an empty string
var isWhat int          // gives `0`
var isWhat float64      // gives `0`
var isWhat complex64    // gives `(0+0i)`
var isWhat bool         // gives `false`
```
- A string in Go stands for any UTF-8 character.
- Strings can be treated as arrays.

> Arrays are 0-indexed.

- Strings are actually aliases for bytes.
- Strings are immutable.

- bytes represents UTF-8 characters.
- A rune represents UTF-32 characters.
- runes are type alias for `int32`.

- You cannot mix types even in the same family when performing operations.
