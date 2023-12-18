# PHP File Handling Cheat Sheet

## Reading from a File

### Reading the Entire File

```php
$file_contents = file_get_contents("filename.txt");
echo $file_contents;
```

### Reading File Line by Line

```php
$lines = file("filename.txt", FILE_IGNORE_NEW_LINES | FILE_SKIP_EMPTY_LINES);

foreach ($lines as $line) {
    echo $line . "<br>";
}
```

### Reading File using fopen and fread

```php
$file_handle = fopen("filename.txt", "r");

while (!feof($file_handle)) {
    $line = fgets($file_handle);
    echo $line;
}

fclose($file_handle);
```

## Writing to a File

### Writing to a File

```php
$file_contents = "This is a new content.";
file_put_contents("newfile.txt", $file_contents);
```

### Writing to a File using fopen and fwrite

```php
$file_handle = fopen("newfile.txt", "w");

fwrite($file_handle, "This is a new content.");

fclose($file_handle);
```

## Appending to a File

```php
$file_contents = "This is additional content.";
file_put_contents("existingfile.txt", $file_contents, FILE_APPEND);
```

## Checking if a File Exists

```php
$filename = "example.txt";

if (file_exists($filename)) {
    echo "File exists!";
} else {
    echo "File does not exist.";
}
```

## Deleting a File

```php
$filename = "file_to_delete.txt";

if (unlink($filename)) {
    echo "File deleted successfully.";
} else {
    echo "Unable to delete the file.";
}
```

## File Permissions

```php
$filename = "example.txt";

// Check if file is readable
if (is_readable($filename)) {
    echo "File is readable.";
}

// Check if file is writable
if (is_writable($filename)) {
    echo "File is writable.";
}
