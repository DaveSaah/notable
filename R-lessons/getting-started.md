# Variables

1. **Categorical variables (qualitative):** Their values can be placed into different groups.
2. **Numerical variables (quantitative):** Mathematical operations can be performed on them. They can be *continuous* or *discrete*.

    - Discrete: Responses arise from a counting process.
    - Continuous: Responses arise from a measuring process.

# Tutorial

## Comments

- Comments are made with `#`.

## Assignment

```R
variable <- expression

# OR
variable = expression
```

## Number Sequence

```R
from:to			    # 1:5
seq(from, to, by)	    # seq(1, 5, .5)

# sample: They give the same output
seq(1, 5, by=.5)
seq(1, 5, b=.5)
seq(1, 5, .5)
```

## Forming a Vector

- The concatenate function, `c` is used.

```R
# Example

c(0, 1, 3, 6, 10)
```

## Concantenating Strings

- Use `paste()` function.

```R
# example

firstNames <- c("David", "John", "Godfred")
lastNames <- c("Saah", "Adenu", "Inkoom")
fullNames <- paste(firstNames, lastNames)

# Returns "David Saah"     "John Adenu"     "Godfred Inkoom"
```

## Note

- In a data frame, use `$` before the column name to get the values in that column.
