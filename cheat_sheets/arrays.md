# PHP Arrays Cheat Sheet

## Indexed Arrays

```php
// Numeric indices
$numeric_array = array("Apple", "Banana", "Orange");

// Shorter syntax (PHP 5.4+)
$short_array = ["Apple", "Banana", "Orange"];
```

## Associative Arrays

```php
$associative_array = array(
    "name" => "John",
    "age" => 25,
    "city" => "New York"
);

// Shorter syntax (PHP 5.4+)
$short_associative_array = [
    "name" => "John",
    "age" => 25,
    "city" => "New York"
];
```

## Accessing Array Elements

```php
$fruits = ["Apple", "Banana", "Orange"];

echo $fruits[0]; // Outputs: Apple

$person = [
    "name" => "John",
    "age" => 25,
    "city" => "New York"
];

echo $person["name"]; // Outputs: John
```

## Modifying Array Elements

```php
$colors = ["Red", "Green", "Blue"];

$colors[1] = "Yellow";

// $colors is now ["Red", "Yellow", "Blue"]
```

## Adding and Removing Elements

```php
$numbers = [1, 2, 3];

// Adding elements
$numbers[] = 4;

// $numbers is now [1, 2, 3, 4]

// Removing elements
unset($numbers[2]);

// $numbers is now [1, 2, 4]
```

## Multidimensional Arrays

```php
$matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
];

echo $matrix[1][2]; // Outputs: 6
```

## Array Functions

```php
$fruits = ["Apple", "Banana", "Orange"];

// Count elements
$count = count($fruits);

// Check if an element exists
$exists = in_array("Banana", $fruits);

// Add elements at the end
array_push($fruits, "Grapes");

// Remove the last element
$last_element = array_pop($fruits);

// Merge arrays
$vegetables = ["Carrot", "Broccoli"];
$combined = array_merge($fruits, $vegetables);
