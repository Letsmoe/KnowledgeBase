# Gyro

## .synx Files
.synx files provide a way of extending the syntax of Gyro by using *ebn*.

### Including foreign syntax
```
#lang gyro
#bind ./main-syntax.synx

new Syntax is Available? -> print(true)
```