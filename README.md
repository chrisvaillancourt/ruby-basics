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

## Control flow

`if`...`elsif`...`else`. the `end` keyword terminates the  block:

```rb
if condition1
  # code
elsif condition2
  # code
else
  # code
end
```

`unless` is the opposite of `if`, it executes if the condition is false:

```rb
unless condition
  # code
end
```

`while` and `until` loops:

```rb
while condition
  # code
end

until condition
  # code
end
```

`for` loops:

```rb
for element in array
  # code
end
```

Ruby typically uses iterators instead of `for` loops.

`case`/`when` is a like a switch/case:

```rb
case variable
when value1
  # code
when value2, value3 # Multiple values
  # code
else
  # code
end
```

