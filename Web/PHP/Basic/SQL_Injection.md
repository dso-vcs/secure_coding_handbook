# SQL Injection

<hr>

## Code lỗi

***VD1:***
```php
    $query = self::$database->exec('DELETE FROM reports WHERE id='. $reportID .' AND user_uid='. $user->uid);
```

***VD2:***
```php
    $query  = "SELECT id, name, inserted, size FROM products WHERE size = '$size'";
    $result = odbc_exec($conn, $query);
```
Đoạn code trên sử dụng nối chuỗi trong câu truy vấn và không kiểm tra đầu vào của người dùng dẫn đến lỗ hổng.

## Code an toàn

**Sử dụng prepared statements**

```php
$query = self::$database->prepare('DELETE FROM reports WHERE user_uid=:uid AND id=:id');
$query->bindValue(':uid', $user->uid);
$query->bindValue(':id', $reportID);
return $query->execute();
```
