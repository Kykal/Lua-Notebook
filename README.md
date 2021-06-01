# Comments
To make a comment while coding in Lua we need to use ``--`` before the comment, i.e.:

```Lua
--This is an inline comment
--[[
This
is a
multiline
comment
]]
```

# Output
``"As a rule, you should use print for quick-and-dirty programs, or for debugging, and write when you need full control over your output"``
-[Programming in Lua 21.1](https://www.lua.org/pil/21.1.html)
```Lua
> print("hello", "Lua"); print("Hi")
  --> hello   Lua
  --> Hi
    
> io.write("hello", "Lua"); io.write("Hi", "\n")
  --> helloLuaHi
```


# Data types
Lua wil know the data type depending what information is inside a variable, but we have the next data types:
```Lua
> boolVarT = true
> boolVarF = false --Booleans

> intVar = 3 --Integer
> floatVar = 5.8 --Float (Lua float precision is 13 decimals)

> stringVar = "Kykal" --String
> longStringVar = [[
  this is
  a very
  long string
  ]] --String (Lua will respect the lines used)
```

### Maxium float precision
The precision of a float variable is 13 decimals, i.e.:
```Lua
> numberVar = 1.1234567890123 --13 decimals
> numberExcedVar = 1.12345678901234 --14decimals

> io.write( numberVar )
  --> 1.1234567890123
> io.write( numberExcedVar )
  --> 1.1234567890123
```

## Lenght of a variable
To know the lenght of a variable we are using just use ``#`` before the calling variable in the ``io.write()/print()`` function.
```Lua
> name = 'Ivánovich'
> io.write( "Ivánovich variable lenght: ", #name )
  --> Ivánovich variable lenght: 9
```

# Operators
```Lua
> io.write( 5 + 9 ) --Addition
  --> 14
> io.write( 10 - 4 ) --Subtraction
  --> 6
> io.write( 25 / 5 ) --Division
  --> 5
> io.write( 10*4 ) --Multiplication
  --> 40
> io.write( 16.4 % 8  ) --Modulus
  --> 2.2
```

# Conditionals
