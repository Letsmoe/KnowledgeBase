# Why?
When managing Monorepos, the most annoying thing is that when pushing your changes to an FTP Server, there are tons of files you didn't actually need.

## How to change that?
Let's say we have this kind of folder structure:

```
root/
	first-app/
		src/
			some-file.js
		dist/
		docs/
		modules/
		test/
	second-app/
		src/
			some-other-file.js
		dist/
		docs/
		modules/
		test/
```

There are a lot of things we don't actually need, in fact, we could simplify it like this:

```
root/
	first-app/
		...dist/
		docs/
	second-app/
		...dist/
		docs/
```

Or:

```
root/
	first-app/
		...dist/
	second-app/
		...dist/
	docs/
		first-app/
			...docs/
		second-app/
			...docs/
```

For that, we could write a config, so that a `Project Manager` can look at everything we built and merge certain items while sorting out others.

```
{
	"directories": {
		"modules": "modules",
		"source": "src",
		"docs": "docs",
		"out": "dist"
	},
	"mergeOptions": {
		"docsMerge": {
			type: "ROOT_FOLDER" | "SUBDIRECTORY",
			folder: string
		},
		"spreadOutIntoOriginal": true | false,
		"removeModules": true | false,
		"removeSource": true | false,
		"moveFromSource": [".*\.html", ".*\.css"]
	}
}
```

Let's make a general directory move setup:

```
some-monorepo/
	dist/
	docs/
		package-1/
		package-2/
	packages/
		package-1/
			src/
			dist/
			docs/
			package.json
			README.md
		package-2/
			src/
			dist/
			docs/
			package.json
			README.md
	LICENSE
	README.md
```