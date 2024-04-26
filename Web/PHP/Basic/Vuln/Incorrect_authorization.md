# Incorrect Authorization

<hr>

## Noncompliant code

```php
$role = $_COOKIES['role'];
if ($role=='admin') {
    DisplayAdminPortal();
}
```

Trong đoạn code trên, thông tin về quyền được lưu trữ trong cookie là không an toàn. Người dùng có thể thay đổi giá trị cookie thành `admin` để truy cập portal.


## Compliant code

Không lưu trữ các thông tin nhạy cảm trên cookie