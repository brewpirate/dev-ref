# Cookies

Cookies are a mechanism for storing data in the remote browser and thus tracking or identifying return users. You can set specific data to be stored in the browser, and then retrieve it when the user visits the site again.

https://www.php.net/manual/en/function.setcookie.php

```php
setcookie(  
    string $name,  
    string $value = "",  
    int    $expires_or_options = 0,  
    string $path = "",  
    string $domain = "",  
    bool   $secure = false,  
    bool   $httponly = false 
): bool
```

Alternative signature available as of PHP 7.3.0 (not supported with named parameters):
```php
setcookie(string $name, string $value = "", array $options = []): bool
```

## Set a cookie

```php
setcookie('name', 'Brad', time() + 86400 * 30); // 86400 = 1 day
```

## ## Get a cookie

```php
if (isset($_COOKIE['name'])) {
  echo $_COOKIE['name'];
}

// or
echo 'Hello ' . htmlspecialchars($_COOKIE["name"]) . '!';  

```

## Delete a cookie

```php
setcookie('name', '', time() - 86400);
```
