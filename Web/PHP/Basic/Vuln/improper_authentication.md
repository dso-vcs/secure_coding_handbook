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