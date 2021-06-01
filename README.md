## Comments
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

## Data types
Lua wil know the data type depending what information is inside a variable, i.e.:

```Lua
name= 'Kykal'
io.write( "1. Data type of 'name' variable: ", type(name) ) --1

intDigit= 4
io.write( "2. Data type of 'intDigit' variable: ", type(intDigit) ) --2

floatDigit= 5.8
io.write( "3. Data type of 'floatDigit' variable: ", type(floatDigit) ) --3
```

Output:
```
1. Data type of 'name' variable: string
2. Data type of 'intDigit' variable: number
3. Data type of 'floatDigit' variable: number
```

### Lenght of a variable
To know the lenght of a variable we are using just use ``#`` before the calling variable in the ``io.write()/print()`` function.
```Lua
name = 'Ivánovich'
io.write( "Ivanovich variable lenght: ", #name )
```
Output:
```
Ivanovich variable lenght: 9
```

### Maxium float precision
The precision of a float variable is 13 decimals, i.e.:
```Lua
numberVar = 1.1234567890123 --13 decimals
numberExcedVar = 1.12345678901234 --14decimals

io.write( numberVar )
io.write( numberExcedVar )
```
Output:
```
1.1234567890123
1.1234567890123
```
