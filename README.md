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
