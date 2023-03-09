# Interfaces

- `interfaces` are a type in Go.
- Interfaces doesn't describe data, they describe behaviour.
- They store method definitions.

```go
// SYNTAX
type interface_name interface {
    // method definitions
}
```
> If you have single method interfaces, naming convention will be `method_name + 'er'`

- Any type that can have a method associated with it can implement an interface.

## Composing Interfaces

```go
// SYNTAX
type interface_name interface {
    // list other interfaces
}
```

> *Read on constructor methods


## Empty Interface 

- It is an interface that has no methods on it.
- Aside the default syntax, it can be created by using `interface{}` as a data type.

> If any of the methods defined has a pointer receiver, the interface must receive a pointer as a value.


### Best Practices

- Use many, small interfaces.
- Don't export interfaces for types that will be consumed.
- Do export interfaces for types that will be used by packages.
- Design functions and methods to receive interfaces whenever possible.

    - If you need access to the underlying data field, take in the concrete type.
    - If you are accepting behaviour providers, take in interface type.
