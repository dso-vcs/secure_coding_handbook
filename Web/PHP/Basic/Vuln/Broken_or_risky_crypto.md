# Broken or risky crypto

<hr>

## Noncompliant code

```php
function encryptData($data, $key) {
    $iv = mcrypt_create_iv(16, MCRYPT_DEV_RANDOM);
    $encryptedData = mcrypt_encrypt(MCRYPT_RIJNDAEL_128, $key, $data, MCRYPT_MODE_CBC, $iv);
    return $encryptedData;
}
```

In this example, the function encryptData() uses the mcrypt_encrypt() function with the MCRYPT_RIJNDAEL_128 algorithm for encryption. This algorithm is considered insecure and vulnerable to attacks.

## Compliant code

```php
function encryptData($data, $key) {
    $iv = openssl_random_pseudo_bytes(16);
    $encryptedData = openssl_encrypt($data, 'aes-256-cbc', $key, OPENSSL_RAW_DATA, $iv);
    return base64_encode($iv . $encryptedData);
}
```

In this example, the encryptData() function uses the openssl_encrypt() function with the aes-256-cbc algorithm for encryption, which is currently considered secure. Additionally, it uses openssl_random_pseudo_bytes() to generate a random initialization vector (IV) for each encryption, which improves the security of the encryption.