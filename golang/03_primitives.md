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


# Note

- When an operation involves two integers, the result will be an integer. In a division operation for instance, the result will only be the integer part of the answer.
    - To avoid data loss, operations that may result into floats should have its operands in the `float32` or `float64` data type.
- Floats have a special notation for exponents. Sample: `2.1e4`, `2E19`, `2.1e-3`, ...
- To get the complex and imaginary parts of a complex number separately:
```go
var comp complex64 = 1 + 10i
realPart, imaginaryPart = real(comp), imag(comp)
```
