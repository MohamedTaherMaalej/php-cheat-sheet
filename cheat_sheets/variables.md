# PHP Variables Cheat Sheet

## Variable Declaration

```php
$variable_name = "Hello, PHP!"; // String variable

$number = 42; // Integer variable

$float_number = 3.14; // Float variable

$boolean = true; // Boolean variable

$null_value = null; // Null variable
```

## Variable Naming Rules

- Variable names in PHP are case-sensitive.
- Must start with a letter or underscore.
- Can only contain letters, numbers, and underscores.
- Cannot start with a number.

## Concatenation

```php
$first_name = "John";
$last_name = "Doe";

$full_name = $first_name . " " . $last_name;
// Result: John Doe
```

## Variable Interpolation

```php
$language = "PHP";

echo "I love $language!";
// Outputs: I love PHP!
```

## Variable Scope

```php
$global_variable = "I am global";

function example_function() {
    $local_variable = "I am local";
    echo $local_variable;
}

example_function(); // Outputs: I am local
echo $global_variable; // Outputs: I am global
```

## Constants

```php
define("MAX_VALUE", 100);
echo MAX_VALUE; // Outputs: 100

// Constants are case-sensitive by default
define("GREETING", "Hello", true);
echo greeting; // Outputs: Hello
```

## Type Casting

```php
$number = "42";
$integer_number = (int)$number;

$float_number = 3.14;
$integer_from_float = (int)$float_number;
```

## Variable Functions

```php
$function_name = "strtoupper";
$text = "hello, php!";

$result = $function_name($text);
// Result: HELLO, PHP!
