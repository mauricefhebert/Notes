---
id: 2kng5xh5ujuy2kf2cjnq6sw
title: Ruby Basic
desc: ""
updated: 1654878364352
created: 1654706632466
---

## Data Types

ruby contain the following data types

- string is equal to a array of characters
- int which is a whole number
- float is a number with decimal point
- array is a collection of data of the same type
- hashes which is a collection of key value pair like a dictionary
- symbol use to define constant string it's on average 1.7x faster then a normal string
- boolean define true or false

## Variable and their scope

Their's 4 type of variable in ruby and each are used in a different scope

### Local variables

A loIal variable name starts with a
lowercase letter or underscore (. lt is
only accessible or have it5 scope
within the bloIk of its initialization.
Once the code block completes,
variable has no scope
<br>
`name = value`
<br>

### Class variables

A class variable name starts with @@
sign.They need to be initialized before
use. A class variable belongs to the
whole class and can be accessible from
anywhere inside the class. lf the value
will be changed at one instance, k will
be changed at every instance.
A class variable is shared by all the
descendent of the class. An uninitialized
class variable will result in an error
<br>
`@@name = value`

### Instance variables

An instance variable name starts with a
@ sign. lt belongs to one instate of the
class and can be accessed from any
instance of the class within a method.
They only have limited access to a
particular instance of a class.
They don't need to be initialize. An
uninitialized instance variable will have
a nil value
<br>
`@name = value`

### Global variables

The global variable is defined globally and can be use anywhere in the programme this type of variable is generally avoided
<br>
`$name = value`
