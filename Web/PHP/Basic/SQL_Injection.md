# SQL Injection

<hr>

## Code lỗi

```php
$query = self::$database->exec('DELETE FROM reports WHERE id='. $reportID .' AND user_uid='. $user->uid);
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
