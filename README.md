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

# Variables
There are ``Global`` and ``Local`` variables. The global ones are the variables that exist along all the program, otherwise, the local variables only exist in a certain part of our program. You can declare a **Local variable** typing ``local`` before its name, if not the variable will be global as default.
```Lua
> nameVar = "Kykal" -- Global variable
> local nameLocalVar = "localKykal" -- Local variable
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
You can not call a bool variable just like that, if you do so Lua will return an error because Lua expected a string, not a boolean, for that you need to convert bool value into a string value, i.e.:
```Lua
myBool = true

> io.write( myBool )
  --> String expected, got boolean

> io.write( tostring(myBool) )
  --> true

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

### Relational operators
```Lua
> -- Greater than
< -- Smaller than
>= -- Grater than or equal to
<= -- Smaller than or equal to
== -- Is equal to
~= -- Not equal to
```
### Logical operators
```Lua
and -- This AND that
or -- This OR that
not --This IS NOT that
```

## Examples
### IF-Statement
The IF-Statement will compare between values that you give, if the comparison is true, will execute the code right below, if not will jump the IF condition
```Lua
if (<comparison>) then
  -- Your code here
end
```

```Lua
> nickname = "Kykal"
> name = "Alan"
> lastName = "Benavides"


> if name == "John" then
>     io.write( "My name is John" )
>   elseif (name == "John") and (lastName == "Smith") then
>     io.write( "My complete name is John Smith" )
>   else
>     local myAge = 21
>     io.write( "My name is ", name," ", lastname, ", my nickname is ", nickname, " and I am", myAge, "years old." )
> end
  --> My name is Alan Benavides, my nickname is Kykal and I am 21 years old.
  
> io.write( tostring(myAge) ) --Turn myAge variable from 'nil' value to '' value (nil value = empty string)
  -->       --We got nothing because myAge variable does not exist outside IF-Statement, so it return a 'nil' that equals to an empty variable.
```

# Loops
## while()
Repeat the code inside the loop **while** the condition is **true**
```Lua
while (<condition>) do
    -- Your code here
end
```

```Lua
> number = 1
> while ( i <= 10 ) do
>   io.write(number)
>   number = number + 1 -- Lua does not support 'number++' nor 'number += 1'
>   if i == 8 then
>     break
>   end
> end
  --> 1234567
```

## repeat-until
It repeat the code inside the loop until the condition is true
```Lua
> repeat
>   -- Your code here
> until (<condition>)
```

```Lua
> repeat
>   io.write( "Is Earth a planet? " )
>   answer = string.lower( io.read() )  -- Obtain an answer and turn all letters into lowercase, this is for an easy use for the condition
> until ( answer == "yes" )
> Earth is a planet

  --> Is Earth a planet? No
  --> Is Earth a planet? Yes
  --> Earth is a planet
```

## for
Repeat the code inside the loop until the condition is reached
```Lua
> for <starting value>, <ending value>, <increment> do  --NOTE: if no increment is typed, increment will be 1 by default.
>   -- Your code 
> end
```

```Lua
> for i=0, 10, 2 do -- From 0 to 10 with an increment of 2
>   print(i)
> end
  --> 0246810
```

# Tables (Arrays)
In Lua we use the term of 'Tables', like 'Arrays' in other languages.
**IMPORTANT:** In Lua, Tables starts from 1 or from the starting point you decide.
```Lua
> myTable {'A', 'B', 'C'}
> io.write( aTable[1] )
  --> A
```
```Lua
> myTable = {} --Declare an empty table
> myTable[-4] = 'ABCD'
> io.write( myTable[-4] )
  --> ABCD
```
