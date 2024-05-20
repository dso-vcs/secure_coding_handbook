# Unverified Password Change

<hr>

## Noncompliant code

```php
$user = $_POST['user'];
$pass = $_POST['pass'];
$checkpass = $_POST['checkpass'];
if ($pass == $checkpass) {
SetUserPassword($user, $pass);
}
```

Đoạn code trên không thực hiện kiểm tra password hiện tại mà trực tiếp cập nhật password mới

## Compliant code

```php
$password = GetPassword();
$user = $_POST['user'];
$curpass = $_POST['curpass'];
$newpass = $_POST['newpass'];
$checkpass = $_POST['checkpass'];
if ($curpass == $password && $checkpass == $newpass) {
    SetUserPassword($user, $newpass);
}
```
