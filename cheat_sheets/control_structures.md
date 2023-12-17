# PHP Control Structures Cheat Sheet

## If Statement

```php
$condition = true;

if ($condition) {
    // Code to be executed if the condition is true
    echo "The condition is true.";
} else {
    // Code to be executed if the condition is false
    echo "The condition is false.";
}
```

## Switch Statement

```php
$day = "Monday";

switch ($day) {
    case "Monday":
        echo "It's the start of the week.";
        break;
    case "Friday":
        echo "TGIF!";
        break;
    default:
        echo "It's a regular day.";
}
```

## While Loop

```php
$counter = 0;

while ($counter < 5) {
    // Code to be executed while the condition is true
    echo $counter;
    $counter++;
}
```

## Do-While Loop

```php
$counter = 0;

do {
    // Code to be executed at least once, then repeated while the condition is true
    echo $counter;
    $counter++;
} while ($counter < 5);
```

## For Loop

```php
for ($i = 0; $i < 5; $i++) {
    // Code to be executed for each iteration of the loop
    echo $i;
}
```

## Foreach Loop

```php
$colors = ["red", "green", "blue"];

foreach ($colors as $color) {
    // Code to be executed for each element in the array
    echo $color;
}
```

## Break and Continue Statements

```php
for ($i = 0; $i < 10; $i++) {
    if ($i == 5) {
        break; // Exit the loop when $i is 5
    }

    if ($i % 2 == 0) {
        continue; // Skip even numbers and continue with the next iteration
    }

    echo $i;
}
