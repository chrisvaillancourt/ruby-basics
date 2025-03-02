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

## Functions

- use the `def` keyword
- parentheses around arguments are often optional but suggested for clarity
- The last evaluated expression is implictitly return, can use `return` keyword but it's typically ommitted.
- methods can be caled with or without parentheses

```rb
def greeting(name1, name2 = "default value") # Optional arguments
  # Method body
  result = "hello, #{name1} and #{name2}"
  return result  # 'return' is optional; the last evaluated expression is returned
end

greeting('topher', 'sam') # "hello, topher and sam"
greeting 'topher', 'sam' # "hello, topher and sam"
greeting('topher') # "hello, topher and default value"
greeting 'topher' # "hello, topher and default value"

def add(a, b)
  a + b
end

add(2, 2) # 4
```

## Classes

```rb
class MyClass
  attr_accessor :attribute1, :attribute2 # Creates getter and setter methods

  def initialize(attr1, attr2)
    @attribute1 = attr1 # Instance variables start with @
    @attribute2 = attr2
  end

  def my_instance_method
    # Use instance variables
    puts "Attribute 1: #{@attribute1}"
  end

  def self.my_class_method
    #Class method, can be called on the class itself.
    puts "I am a class method."
  end

end

obj = MyClass.new("value1", "value2")
obj.my_instance_method  # Accessing an instance method
puts obj.attribute1       # Accessing an attribute (using the getter)
obj.attribute2 = "new value" # Setting an attribute (using the setter)
MyClass.my_class_method # Calling class method.
```

- instance variables start with `@`
- `attr_accessor`, `attr_reader`, `attr_writer` are meta programming features
  - `attr_accessor` creates a getter and setter method
  - `attr_reader` only creates a getter
  - `attr_writer` only creates a setter
- `self` TODO
