# Installing/Using your package

You have **two options** to install/provide your package:
 - **Option 1:** laravel uses your package (recommended)
 - **Option 2:** an other package uses your package
 
## **Option 1:** laravel uses your package
The recommended way is, to use your package in your laravel installation.

You need to add following line to your `composer.json` of the laravel project:

 - **Linux:** `/opt/laravel/composer.json`
 - **Windows:** `D:/laravel/composer.json`
```json
{
   // Your content of the file
   
   "require": {
      // Other used packages
      
      "demo/example": "dev-master"
   }
}
```

Additional you can use `require-dev` instead of `require` - The `require-dev` are mostly build tools on your development system and will not installed, if you use a productive system.

## **Option 2:** an other package uses your package
That is easier than eating pommes frites!

Like **Option 1**, you only need to add the reference in your own package's `composer.json`. You only set the reference not in the laravel's `composer.json`, you set these on the package itself:
 - **Linux:** `/opt/laravel/packages/demo/example/composer.json`
 - **Windows:** `D:/laravel/packages/demo/example/composer.json`
```json
{
   // Your content of the file
   
   "require": {
      // Other used packages
      
      "demo/example2": "dev-master"
   }
}
```

## Update before using your package!
Yep, you have **changed** a `composer.json` (irrelevant, if the composer file is from your laravel project or from your package)!
Tell composer, the new configuration:

```
  composer update
```

## Usage
You already have defined the `Example` class  in your package `demo/example`, now use it on your complete laravel project, you only must call these classes in PHP.

Add following `usage` to your PHP file, you wan't to use:

```php
    use demo\example\Example
```

And now, you can use your `Example` class:

```php
    new Example();
```

If you don't know, where you can place it, try it out to create a `Route`:

 - **Linux:** `/opt/laravel/routes/web.php`
 - **Windows:** `D:/laravel/routes/web.php`
```php
<?php
    use demo\example\Example
    
    /*
    |--------------------------------------------------------------------------
    | Web Routes
    |--------------------------------------------------------------------------
    |
    | Here is where you can register web routes for your application. These
    | routes are loaded by the RouteServiceProvider within a group which
    | contains the "web" middleware group. Now create something great!
    |
    */
    
    Route::get('/example', function () {
        new Example();
    });

    
    /* Your other routes... */
```

Now, you can test it on your Site: http(s)://yourdomain.com/`example`!

----
<table width="100%">
  <tr>
    <th>
      <a href="package.md">[ < Previous ] Create your first package</a>
    </th>
  </tr>
</div>
