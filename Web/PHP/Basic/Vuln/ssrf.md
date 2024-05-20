# SSRF

<hr>

## Noncompliant code

```php
$url = $_GET['url'];
$file = file_get_contents($url);
echo $file;
```

In this noncompliant code, an attacker can pass a malicious URL through the “url” parameter in the GET request and the server will make a request to that URL using the file_get_contents() function. This allows the attacker to perform unauthorized actions on behalf of the server.

## Compliant code

```php
$url = $_GET['url'];
if (filter_var($url, FILTER_VALIDATE_URL) === FALSE) {
    echo "Invalid URL";
} else {
    $file = file_get_contents($url);
    echo $file;
}
```
