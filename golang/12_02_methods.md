# Methods

- A method is a function that is executing in a known context.
- A known context in Go is any data type.

## SYNTAX

```go
func (known_context) method_name() return_types {
    // some code
}
```

## Example

```go
func main() {
	g := greeter{
		greeting: "Hello",
		name:     "David",
	}

	g.greet()
}

type greeter struct {
	greeting string
	name     string
}

// value receiver example
func (g greeter) greet() {
	fmt.Println(g.greeting, g.name)
}

// pointer receiver example
func (g *greeter) greet() {
	fmt.Println(g.greeting, g.name)
}
```

## Note

- Types can be created using: `type type-name data-type`. E.g. `type counter int`.
- The known context can either be a value receiver or a pointer receiver.
