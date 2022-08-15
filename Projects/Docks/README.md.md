# Docks
A general purpose templating engine written in JavaScript.

## Why?
`Docks` is an intermediary application that handles file input and output converting any given file to a representation containing transformed information about the input file.

## Syntax
The Syntax of `Docks` is quite simple.
Internally `Docks` uses [[Gyro]] as base language but can use any application that can be run Synchonously or Asynchronously.

Let's look at an example Markdown file.
```markdown
# Heading

This is some text containing a {{variable}}
```


## Containers
Every part of the syntax of `docks` is based upon the principle of `Containers` which are basic structures that can `evaluate`, `display` or make use of information in some other way.

### Output Containers
Are the base of any file containing `docks` syntax. The information inside this container will be displayed (rendered at the specific position).

```markdown
# Heading

This is some {{Output}}
```

Will be converted to:

```markdown
# Heading

This is some Output
```
Normally, everything inside an output container will be interpreted as a variable or constant, if the name of that variable can not be found however, it will be assumed to be a string.

### Evaluation Containers
Will execute what's inside of them. Normally the code inside will be evaluted using [[Gyro]] but a directive can be used to specify otherwise.

```markdown
{[(/usr/bin/python)
x = 5;
text = "This is some python code."

print(text)
](assignedVariable)}

This will output to {{assignedVariable}}...
```

The result of an evaluation will have to be written to the stdout of the given application for it to be rendered. A variable assignment directive can be used however to capture the output of an evaluation context and store it for later use. 