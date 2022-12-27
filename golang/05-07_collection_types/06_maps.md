# Maps

- A map takes a key and 'maps' that to some value. (more like dictionaries in python.)

```go
// Example
statePopulations := map[string] int {
    "state1" : 123,
    "state2" : 345,
    "state3" : 567
}
```

# Constraints

- We can only map a key of one type to a value of one type. (refer to the example above.)
- The data type chosen as a key must testable for equality.


# Creating Maps

```go
// SYNTAX 1

variable := map[key_data_type] value_data_type {
    key : value,
    key : value,
    ...
}

// SYNTAX 2

variable := make(map[key_data_type]value_data_type)
variable = map[string] int {
    key : value,
    key : value,
    ...
}
```

# Manipulating Maps

## Get Value From Map

```go
// syntax
map_name[key_name]

// example
population["Ghana"]
```

## Add (or Update) Value To (of) Map

```go
map_name[key_name] = value
```

## Delete Entries From A Map

```go
delete(map_name, key)
```

## Length of a map

```go
len(map_name)
```

# Note

- The return order of a map is not guaranteed.
- Just like slices, underlying data of maps is passed by reference.
    - If maps are assigned to different variables, the new and old all point to the same data in memory.

# When Key is not available
- When a key that is not found in the map is used, the value returned is 0. The way to check if indeed a key is not available in a map is to use a comma syntax. E.g.

```go
number, ok = statePopulations["no key"]
```
- The value of number is 0.
- The value of `ok` is `false`. (i.e the key does not exist inside the map.)
- If the value of `ok` is `true`, then the key exists.
