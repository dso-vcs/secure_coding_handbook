# Broken or risky crypto

<hr>

## Code lỗi

```php
function encryptData($data, $key) {
    $iv = mcrypt_create_iv(16, MCRYPT_DEV_RANDOM);
    $encryptedData = mcrypt_encrypt(MCRYPT_RIJNDAEL_128, $key, $data, MCRYPT_MODE_CBC, $iv);
    return $encryptedData;
}
```

Đoạn code encrypt trên sử dụng thuật toán 

## Safe code