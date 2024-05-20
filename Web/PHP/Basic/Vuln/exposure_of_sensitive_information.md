# Exposure of Sensitive Information

<hr>

## Noncompliant code

***Eg: Lưu thông tin log nhạy cảm vào file error log có khả năng bị truy xuất bởi người dùng thường***

```php

//exposing sensitive information in error log

    function processUserInput($input) {
        // Process user input
        // ...

        // Log error with sensitive information
        error_log("Error processing user input: $input");
    }
```

In this noncompliant code example, the function processUserInput() logs an error message that includes the user input directly into the error log. This can potentially expose sensitive information to anyone who has access to the error log file, including unauthorized users.


## Compliant code

```php

// avoiding exposure of sensitive information in error log

    function processUserInput($input) {
    // Process user input
    // ...
    
    // Log error without sensitive information
    error_log("Error processing user input"); // Log generic error message
    }

```

