# Readme
This folder includes all projects that are either in planning, already done or which are currently being worked on.

## [[Projects/Gyro/README|Gyro]]
A compiled, statically typed programming language.
### [[Gyro/Math/README|Gyro/Math]]
A math library for [[Gyro/README|Gyro]].	

## [[MarkdownPlus/README|MarkdownPlus]]
A Markdown transpiler implementing [[Gyro/README|Gyro]] to extend it's basic syntax and using [[Templating Language]] to convert from Markdown with variables to standard Markdown.
```
{{
	const x = "title";
}}

# This is a {{ x }}!
```

## [[Snowblind/README|Snowblind]]
A compiled, reactive JavaScript frontend.

## [[Templating Language]]
A general templating language that can be used to create templates by including a code block syntax.
```
{{#/usr/bin/python
	print("Hello World!");
}}
```
Will be converted to:
```
Hello World!
```