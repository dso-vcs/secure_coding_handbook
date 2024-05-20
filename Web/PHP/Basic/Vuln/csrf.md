# CSRF 

<hr>

## Noncompliant code

```php
<form action="transfer.php" method="post">
    <input type="hidden" name="amount" value="1000">
    <input type="submit" value="Transfer Funds">
</form>
```

In this noncompliant example, a form is submitted to a PHP script called “transfer.php” that transfers funds. The amount to be transferred is sent as a hidden form field called “amount”. However, this code does not include any CSRF protection, meaning that an attacker could create a form on a different website that submits the same data to “transfer.php”, tricking the user into transferring funds without their knowledge.

## Compliant code

- Using CSRF token inside the form

```php
<?php
    session_start();
    $_SESSION['token'] = bin2hex(random_bytes(32));
?>

<form action="transfer.php" method="post">
    <input type="hidden" name="amount" value="1000">
    <input type="hidden" name="token" value="<?php echo $_SESSION['token']; ?>">
    <input type="submit" value="Transfer Funds">
</form>
```

- Using A Double-Submit Cookie
- Set `Samesite Cookie` to `Strict`
