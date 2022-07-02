# Dialects
```gyro
extend syntax by Ternary {
	[(condition: any)] ? [(is_true: any)] : [(is_false: any)]
} implements {
	if (condition) {
		return is_true;
	}
	return is_false;
}
```
