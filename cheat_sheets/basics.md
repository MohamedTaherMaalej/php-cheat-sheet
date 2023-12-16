# PHP Basics Cheat Sheet

## Comments

```php
// This is a single-line comment

/*
   This is a
   multi-line comment
*/
```

## Variables

```php
$variable_name = "Hello, PHP!"; // String variable

$number = 42; // Integer variable

$float_number = 3.14; // Float variable

$boolean = true; // Boolean variable

$null_value = null; // Null variable
```

## Data Types

```php
$string = "Hello, PHP!"; // String

$integer = 42; // Integer

$float = 3.14; // Float

$boolean = true; // Boolean

$null_value = null; // Null
```

## Operators

```php
// Arithmetic Operators
$result = 10 + 5; // Addition
$result = 10 - 5; // Subtraction
$result = 10 * 5; // Multiplication
$result = 10 / 5; // Division

// Assignment Operators
$variable = 5;
$variable += 3; // $variable is now 8

// Comparison Operators
$is_equal = (10 == 5); // false
$is_identical = (10 === "10"); // false

// Logical Operators
$and_result = (true && false); // false
$or_result = (true || false); // true
$not_result = !true; // false
```

## Conditional Statements

```php
$number = 42;

if ($number > 0) {
    echo "Positive number";
} elseif ($number < 0) {
    echo "Negative number";
} else {
    echo "Zero";
}
```

## Loops

```php
// For Loop
for ($i = 0; $i < 5; $i++) {
    echo $i;
}

// While Loop
$counter = 0;
while ($counter < 3) {
    echo $counter;
    $counter++;
}

// Foreach Loop
$colors = ["red", "green", "blue"];
foreach ($colors as $color) {
    echo $color;
}
```

## Functions

```php
function greet($name) {
    return "Hello, $name!";
}

echo greet("John"); // Outputs: Hello, John!

