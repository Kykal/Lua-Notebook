# lua

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
io.write( "Data type of 'name' variable: ", type(name) )

digit= 4
io.write( "Data type of 'digit' variable: ", type(digit) )
```

Output:
```
Data type of 'name' variable: string
Data type of 'digit' variable: number
```

### Lenght of a variable
To know the lenght of a variable we are using just use ``#`` before the variable in the output function.
```Lua
name = 'Ivanovich'
io.write( "Ivanovich variable lenght: ", #name )
```
Output:
```
Ivanovich variable lenght: 9
```
