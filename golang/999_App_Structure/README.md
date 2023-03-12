# File Structure in Go Apps

## Flat structure

- Keep all the code in the same package.

## Layered Architecture

- Group by function:

    1. User interface
    2. Core logic
    3. External dependences

- Package name is the folder name.
- Code files in the root directory are in the main package.

## Group By Modules

- Everything about a particular aspect of the application is placed in the same package and stored in the same folder.

# Things To Note

- A packages is a grouping unit of code pieces.
- The main types of packages are:

    - Executable packages ('main')
    - Non-Executable packages (anything apart of 'main')

## Packaging Best Practices

- Package name should be the same at its directory.
- No camel or snake case for package name.
- Packages should be small and many (files).
- There should be minimum directory nesting.

## Package Scopes

- Block
- Unexported
- Exported

> Circular references are not allowed in packages.

