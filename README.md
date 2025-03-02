# Ruby Basics

## core concepts and syntax

- everythinng is an object
- create a variable by assigning a value to a name (like python)
- double quote strings allow for variable interpolation:

```rb
name = 'topher'
greeting = "hello #{name}"
```

- `nil` represents absent vales but they aren't equal to empty strings or 0 like in JS.
- Ruby uses hashes for key value pairs: `{ key1: "value", key2: 2}`
  - (like dictionaries in python)
- symbols `:my_symbol` are immutable strings, typically used as keys in hashes
  - more efficient than strings because a symbolk always refers to the same object in memory

