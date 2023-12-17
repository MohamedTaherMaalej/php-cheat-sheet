# PHP Functions Cheat Sheet

## Function Declaration

```php
function greet() {
    echo "Hello, PHP!";
}

greet(); // Outputs: Hello, PHP!
```

## Function Parameters

```php
function greet_user($name) {
    echo "Hello, $name!";
}

greet_user("John"); // Outputs: Hello, John!
```

## Default Parameter Values

```php
function greet_user($name = "Guest") {
    echo "Hello, $name!";
}

greet_user(); // Outputs: Hello, Guest!
greet_user("Alice"); // Outputs: Hello, Alice!
```

## Returning Values

```php
function add($a, $b) {
    return $a + $b;
}

$result = add(3, 5);
echo $result; // Outputs: 8
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

## Anonymous Functions (Closures)

```php
$add = function ($a, $b) {
    return $a + $b;
};

$result = $add(3, 5);
echo $result; // Outputs: 8
```

## Variable Functions

```php
$function_name = "strtoupper";
$text = "hello, php!";

$result = $function_name($text);
// Result: HELLO, PHP!
```

## Recursion

```php
function factorial($n) {
    if ($n <= 1) {
        return 1;
    } else {
        return $n * factorial($n - 1);
    }
}

$result = factorial(5);
echo $result; // Outputs: 120
