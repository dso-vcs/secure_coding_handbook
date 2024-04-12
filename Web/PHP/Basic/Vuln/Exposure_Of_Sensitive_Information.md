# Exposure of Sensitive Information

<hr>

## Code lỗi

***VD1: Lưu thông tin log nhạy cảm vào file error log có khả năng bị truy xuất bởi người dùng thường***

```php

//exposing sensitive information in error log

    function processUserInput($input) {
        // Process user input
        // ...

        // Log error with sensitive information
        error_log("Error processing user input: $input");
    }
```

Hàm `processUserInput()` ghi lại thông báo lỗi bao gồm dữ liệu nhập trực tiếp của người dùng vào nhật ký lỗi. Điều này có khả năng tiết lộ thông tin nhạy cảm cho bất kỳ ai có quyền truy cập vào tệp nhật ký lỗi, kể cả người dùng trái phép


## Safe code

```php

// avoiding exposure of sensitive information in error log

    function processUserInput($input) {
    // Process user input
    // ...
    
    // Log error without sensitive information
    error_log("Error processing user input"); // Log generic error message
    }

```

