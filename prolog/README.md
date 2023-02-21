# Prolog

- Been around since 1970.
- Applications

    - relational databases
    - mathematical logic
    - NLP
    - other areas of AI

## Features

- Specifies some facts about objects and their relationships.
- Defines some rules about objects and their relationships.
- Asks questions about objects and their relationships.
- The facts and the rules goes into a file called a database.
- The questions are queries to the database.

## Syntax

- The names of all relationships and objects must begin with a lower-case letter.
- The relationship is written first, and the objects are written separated by commas, ad the objects are enclosed by a pair of round brackets.
- Every statement must end with a full stop (`.`).

> **arity** is the number of objects involved in a predicate.

### Variables

- Variable names start with an uppercase letter.
- They can be used to find the response of a relationship.
- The scope of a variable is within a rule.

```prolog
?- likes(john, X).
```

> If the object has a relationship with multiple objects, enter `;` to reveal the rest of the objects.

### Questions

- A question looks like a fact.
- It is indicated by `?-`.

```prolog
?- owns(mary, book)     % is it the case that mary owns the book?
```

### Rules

- They are used to show that a fact depends on other facts.
- `if` is used to express a rule.
- E.g. "I use an umbrella, if there is rain."
- The pattern is `q if p`.

```prolog
/* Examples
## E.g. 1

X is a bird if:
    X is an animal, and
    X has feathers.

## E.g. 2

John likes anyone who likes wine.

*/

likes(john, X) :- likes(X, wine).
```

## Setting Up Prolog

- Working directory can be specified using: `directory($path_dir)`.
- Choose a database to use with: `consult($file_path)`.

## Things To Note

- Objects cannot start with uppercase letters.
- An object is an argument to a predicate.

> An object (in OOP) is data structure that his its own methods and attributes.

- A fact in logic is a proposition. E.g.

```prolog
% "John owns the book."
owns(john, book)

% "The jewel is valuable"
valuable(jewel)
```

- Databases are saved with a `.pl` extension.


## Program Notes

```prolog
?- male(kweku), female(jackie).     % add statement

```
