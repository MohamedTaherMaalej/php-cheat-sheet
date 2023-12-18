# PHP Classes and Objects Cheat Sheet

## Class Declaration

```php
class Car {
    // Properties
    public $brand;
    public $model;
    public $color;

    // Constructor
    public function __construct($brand, $model, $color) {
        $this->brand = $brand;
        $this->model = $model;
        $this->color = $color;
    }

    // Method
    public function start() {
        echo "The $this->color $this->brand $this->model is starting.";
    }
}
```

## Object Instantiation

```php
// Creating an object
$my_car = new Car("Toyota", "Camry", "Blue");

// Accessing properties
echo $my_car->brand; // Outputs: Toyota

// Calling a method
$my_car->start(); // Outputs: The Blue Toyota Camry is starting.
```

## Inheritance

```php
class ElectricCar extends Car {
    // Additional property
    public $battery_range;

    // Overriding method
    public function start() {
        echo "The $this->color $this->brand $this->model with a range of $this->battery_range miles is starting.";
    }
}

// Creating an object of the derived class
$my_electric_car = new ElectricCar("Tesla", "Model S", "Red");
$my_electric_car->battery_range = 300;

// Calling the overridden method
$my_electric_car->start();
// Outputs: The Red Tesla Model S with a range of 300 miles is starting.
```

## Encapsulation

```php
class BankAccount {
    private $balance;

    // Getter
    public function getBalance() {
        return $this->balance;
    }

    // Setter
    public function deposit($amount) {
        $this->balance += $amount;
    }
}

// Creating an object
$account = new BankAccount();

// Accessing private property using getter
$balance = $account->getBalance();

// Modifying private property using setter
$account->deposit(1000);
```

## Static Methods and Properties

```php
class MathUtility {
    // Static property
    public static $pi = 3.14;

    // Static method
    public static function square($number) {
        return $number * $number;
    }
}

// Accessing static property
echo MathUtility::$pi; // Outputs: 3.14

// Calling static method
$result = MathUtility::square(4); // $result is now 16
