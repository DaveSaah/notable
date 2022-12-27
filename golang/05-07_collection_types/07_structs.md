# What are they?

- It gathers information together that are related to one concept.
- There are no constraints on the type of data that can be stored inside a `struct`.

# Creating a Struct
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

# Using a Struct

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

- Another way to instantiate a struct is to use the positional syntax.
    - The values in the struct are declared in the same order it was defined. (Think of the differences as keyless arguments of a function vs keyword arguements)

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

# Getting Values From a Struct

- Dot (.) syntax is used to get the corresponding fields inside a struct.

```go
// Syntax
variable_name.field_name

// Example
fmt.Println(person1.name)   // returns the name of person1
```

# Naming Conventions

- Variable naming conventions still holds for structs.

# Anonymous Struct

- 
