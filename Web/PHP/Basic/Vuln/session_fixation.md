# Session Fixation

<hr>

## Noncompliant code

```php
session_start();
if (isset($_POST['username']) && isset($_POST['password'])) {
    $username = $_POST['username'];
    $password = $_POST['password'];
    if (authenticate($username, $password)) {
        $_SESSION['authenticated'] = true;
        $_SESSION['username'] = $username;
  }
}
```

In the noncompliant code above, the session ID is generated when session_start() is called. However, the authenticated session is not regenerated after a successful login. This leaves the user’s session vulnerable to session fixation attacks.

## Compliant code

```php
session_start();
if (isset($_POST['username']) && isset($_POST['password'])) {
    $username = $_POST['username'];
    $password = $_POST['password'];
    if (authenticate($username, $password)) {
        // Regenerate session ID after successful login
        session_regenerate_id();
        $_SESSION['authenticated'] = true;
        $_SESSION['username'] = $username;
  }
}
```

In the compliant code above, the session_regenerate_id() function is called after a successful login to regenerate the session ID. This ensures that the user’s session is protected against session fixation attacks.