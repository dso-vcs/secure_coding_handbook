# Use of Hardcoded password

<hr>

## Noncompliant code

```php
// This code includes a hard-coded password directly in the script
$password = "MyHardCodedPassword123";
$connection = mysqli_connect("localhost", "myuser", $password, "mydatabase");
```

The password is directly included in the script, making it vulnerable to exposure

## Compliant code

```php
// This code stores the password in a separate configuration file with restricted access
$config = parse_ini_file("/etc/myapp/config.ini");
$connection = mysqli_connect("localhost", "myuser", $config['db_password'], "mydatabase");
```

The compliant code example addresses this issue by storing the password in a separate configuration file with restricted access. This helps to protect the password from being easily discovered by attackers and limits its exposure to authorized personnel who have access to the configuration file.
