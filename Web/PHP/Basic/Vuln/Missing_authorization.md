# Missing Authorizaton

<hr>

## Noncompliant code

```php
function runEmployeeQuery($dbName, $name){
    mysql_select_db($dbName,$globalDbHandle) or die("Could not open Database".$dbName);
    
    $preparedStatement = $globalDbHandle->prepare('SELECT * FROM employees WHERE name = :name');
    $preparedStatement->execute(array(':name' => $name));
    return $preparedStatement->fetchAll();
}
/.../

$employeeRecord = runEmployeeQuery('EmployeeDB',$_GET['EmployeeName']);
```

Hàm `runEmployeeQuery()` trong đoạn code trên không kiểm tra quyền người dùng trước khi gọi. 

## Compliant code

```php
function runEmployeeQuery($dbName, $name){
    mysql_select_db($dbName,$globalDbHandle) or die("Could not open Database".$dbName);
    
    $preparedStatement = $globalDbHandle->prepare('SELECT * FROM employees WHERE name = :name');
    $preparedStatement->execute(array(':name' => $name));
    return $preparedStatement->fetchAll();
}
/.../

//kiểm tra quyền của người dùng trước khi thực hiện hàm 
if(checkRoleUser($SESSION['user'])=='admin'){
    $employeeRecord = runEmployeeQuery('EmployeeDB',$_GET['EmployeeName']);
}
```