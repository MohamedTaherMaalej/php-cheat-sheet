# PHP Database Access Cheat Sheet

## Connecting to a Database

```php
$servername = "localhost";
$username = "username";
$password = "password";
$dbname = "database_name";

// Create connection
$conn = new mysqli($servername, $username, $password, $dbname);

// Check connection
if ($conn->connect_error) {
    die("Connection failed: " . $conn->connect_error);
}
```

## Executing SQL Queries

### SELECT Query

```php
$sql = "SELECT column1, column2 FROM tablename WHERE condition";
$result = $conn->query($sql);

if ($result->num_rows > 0) {
    while ($row = $result->fetch_assoc()) {
        echo "Column1: " . $row["column1"]. " - Column2: " . $row["column2"]. "<br>";
    }
} else {
    echo "0 results";
}
```

### INSERT Query

```php
$sql = "INSERT INTO tablename (column1, column2) VALUES ('value1', 'value2')";

if ($conn->query($sql) === TRUE) {
    echo "Record inserted successfully";
} else {
    echo "Error: " . $sql . "<br>" . $conn->error;
}
```

### UPDATE Query

```php
$sql = "UPDATE tablename SET column1 = 'new_value' WHERE condition";

if ($conn->query($sql) === TRUE) {
    echo "Record updated successfully";
} else {
    echo "Error: " . $sql . "<br>" . $conn->error;
}
```

### DELETE Query

```php
$sql = "DELETE FROM tablename WHERE condition";

if ($conn->query($sql) === TRUE) {
    echo "Record deleted successfully";
} else {
    echo "Error: " . $sql . "<br>" . $conn->error;
}
```

## Prepared Statements

```php
$stmt = $conn->prepare("INSERT INTO tablename (column1, column2) VALUES (?, ?)");
$stmt->bind_param("ss", $value1, $value2);

$value1 = "new_value1";
$value2 = "new_value2";
$stmt->execute();

echo "Record inserted successfully";

$stmt->close();
```

## Closing the Database Connection

```php
$conn->close();
```

This cheat sheet provides information on connecting to a database, executing SELECT, INSERT, UPDATE, and DELETE queries, using prepared statements, and closing the database connection in PHP. Customize it based on your specific database and needs, and ensure to use best practices such as prepared statements to prevent SQL injection.
