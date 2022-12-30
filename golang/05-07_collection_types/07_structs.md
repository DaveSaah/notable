# Structs

## What are they?

- It is a collection of different data types that describe a single concept.
- There are no constraints on the type of data that can be stored inside a `struct`.

## Creating a Struct

```go
// Syntax
type variable_name struct {
    // data type declarations
}

// example
type person struct {
    name string
    age int
    siblings []string
}
```

## Using a Struct

```go
// example
person1 := person {
    name: "David Saah",
    age: 20,
    siblings: []string {
        "Linux",
        "Golang",
        "Julia",
        "Python",
    },
}
```

### Positional Declaration For Structs Usage

- Another way to instantiate a struct is to use the positional syntax.
- The values in the struct are declared in the same order it was defined.

```go
// Example
person2 := person {
    "DaveSaah",
    20,
    []string {
        "Github",
        "Charm",
        "Bashbunni",
    }
}
```
> It is recommended to use field names when creating struct objects to prevent semantic bugs in the future.

## Getting Values From a Struct

- Dot (.) syntax is used to get the corresponding fields inside a struct.

```go
// Syntax
variable_name.field_name

// Example
fmt.Println(person1.name)   // returns the name of person1
```
### Advantages of Using Keywords in Creating Struct Objects

- If a defined struct field is not given a value when a struct object is created, there is no error and it given a zero value.

```go
// example
type versionControl struct {
    name string
    age int
    family []string
}

// Creating an object
var github = versionControl {
    name: "Github",
    age: 200,
}

fmt.Println(versionControl.family)  // prints []
```
- It makes room for changing struct content without having to change its usage. This makes the program robust and change proof.

### When To Use Positional Declaration for Structs Usage

- When creating an anonymous struct.
- When a struct has a short lifespan.

## Naming Conventions

- Variable naming conventions still holds for structs.

## Note

- As opposed to `maps`, `structs` are value data types. This means when a struct is assigned to a variable, it points to a different location in memory. A change in the new struct does not affect the old.

> Unlike `maps` and `slices`,`structs` refer to independent data.

- To point to the same memory address of a `struct`, use the address operator, `&`.

```go
var mainStruct = struct{name string}{name: "DaveSaah"}
var copyStruct = &mainStruct

// Changing the data in `copyStruct` affects `mainStruct`
```

