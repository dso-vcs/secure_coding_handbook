# Path Traversal

<hr>

## Noncompliant code
***VD1: Path traversal thông qua upload file***

```php
public function uploadPhoto(): bool
    {
        return User::addPhoto($_FILES['file']['name']);
    }
```

Đoạn code trên không thực hiện kiểm tra tên file đầu vào

***VD2: Path traversal file include***

```php
    $template = $_COOKIE['TEMPLATE'];
    include ( "/home/users/phpguru/templates/" . $template );
```

## Compliant code

**Option 1:**

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

**Option 2:**

Sử dụng hàm `realpath()` 