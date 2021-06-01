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
Lua wil know the data type depending what information is inside a variable, but we have the next data types:
```Lua
boolVarT = true
boolVarF = false --Booleans

intVar = 3
floatVar = 5.8

string = "Kykal"
longString = [[
this is
a very
long string
]]
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
