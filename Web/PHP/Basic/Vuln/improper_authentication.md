# Improper Authentication

<hr>

## Noncomplaint code

***Example 1: Weak Password***
```php
$password = $_POST['password'];
if ($password === 'password123') {
    // Allow access
} else {
    // Deny access
}
```
Use of a weak password that can easily be guessed by attackers

***Example 2: Hardcoded Credentials***
```php
$username = 'admin';
$password = 'password';
if ($_POST['username'] === $username && $_POST['password'] === $password) {
    // Allow access
} else {
    // Deny access
}
```
Use of hardcoded credentials that can be easily discovered by attackers

## Complaint code

The compliant code examples address these issues by using strong password hashing algorithms and storing user credentials securely in a database.

***Example 1: Weak Password***
```php
$password = $_POST['password'];
if (password_verify($password, $hashedPassword)) {
    // Allow access
} else {
    // Deny access
}
```

The first example uses the password_verify function to compare the user’s input password with a hashed password stored in the database. 

***Example 2: Hardcoded Credentials***
```php
$username = $_POST['username'];
$password = $_POST['password'];

// Validate the user's credentials against a secure database
if (validateCredentials($username, $password)) {
    // Allow access
} else {
    // Deny access
}
```

The second example validates the user’s credentials against a secure database, rather than using hardcoded credentials in the application code.