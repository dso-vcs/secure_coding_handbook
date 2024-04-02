# Path Traversal

<hr>

## Code lỗi

```php
public function uploadPhoto(): bool
    {
        return User::addPhoto($_FILES['file']['name']);
    }
```

Đoạn code trên không thực hiện kiểm tra tên file đầu vào

## Code an toàn

Sử dụng hàm `basename()` lấy tên file cuối cùng trong đường dẫn. VD: **`basename("/etc/passwd") = "passwd"`**

```php
public function uploadPhoto(string $hashKey, Request $request): bool
    {
        $post = $request->getParsedBody();
        $user = User::getCurrentUser($hashKey);
        $userDir = $this->service->getUserDir($user);
        $tmp_name = $_FILES['photo']['tmp_name'];
        $name = basename($_FILES['photo']['name'] . '-' . $user->uid);
        $fileSize = $post['photo']['size'];

        if ($userDir && CheckDataService::isValidImage($fileSize) && $this->service->isValidPath($hashKey)
        ) {
            $destination = $userDir . 'images';
            move_uploaded_file($tmp_name, "$destination/$name");
            return User::addPhoto($destination);
        }
        return false;
    }
```

