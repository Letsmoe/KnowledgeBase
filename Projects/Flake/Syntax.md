# Syntax
Since most programming languages support the definition of functions, and the ones that do not can define their own set of methods for executing something, we can provide a way of testing that is significantly easier to grasp because of its uniformity.

## Javascript
```js
function main() {
	return 42;
}

let result = main()

assert(result === 42);
```

## Python
```python
def main():
	return 42

result = main()
assert(result == 42)
```

## Scheme
```scheme
(define (main) 42)

(define result (main))

(assert (equal result 42))
```

## Gyro
```gyro
const main = func() {
	return 42;
}

const result: number = main();

assert(result == 42);
```

## PHP
```php
function main() {
	return 42;
}

$result = main();

assert($result == 42);
```

## Lua
```lua
function main ()
	return 42
end

result = main()
assert(result == 42)
```

## Heck, even Bash!
```bash
function main {
	echo 42
}

result=$(main)
assert $result 42
```