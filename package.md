# Create your first package

Here comes the magic. Create your own Package!

Navigate to your `packages` folder:

**Linux**
```
 $ cd packages
```
 
 **Windows**
```
  cd packages
```

You now on following path:
 - **Linux:** `/opt/laravel/packages`
 - **Windows:** `D:/laravel/packages`

Create now your own package with your name. For sample, we using the name `demo/example`.

**Linux**
```
  $ mkdir -p demo/example/src
```

**Windows**
```
  mkdir demo\example\src
```

You now created following structure:

**Linux**
```
 /opt
   /laravel
     /packages
       /demo
         /example
           /src
```

**Windows**
```
 D:/
   laravel/
     packages/
       demo/
         example/
           src
```

Go into your package:

**Linux**
```
  $ cd demo/example
```

**Windows**
```
  cd demo/example
```

And now, you create the file `composer.json` with following content:

> **NOTE:** please update the fields (for example, `name`, `description`, `authors` and `psr-4` with your informations`)

```
{
    "name": "demo/example",
    "description": "Example laravel package",
    "type": "library",
    "license": "MIT",
    "authors": [
        {
            "name": "Yor Name",
            "email": "address@example.com"
        }
    ],
    "minimum-stability": "dev",
	  "require-all": true,
		"autoload": {
		"psr-4": {
				"demo\\example\\": "src/"
		}
	}
}
```

The basic of your package is finished!

For testing, you can create your first class. We call it `Example`:

 - **Linux:** /opt/laravel/packages/demo/example/src/Example.php
 - **Windows:** D:/laravel/packages/demo/example/src/Example.php
 
And place following content:
 
```php
<?php
	namespace example\demo;
  
  class Example {
  	public function __construct() {
    	  print 'My example package example\demo\Example!';
     	} 
   }
```

The structure of yor package is now as followed:

**Linux**
```
 /opt
   /laravel
     /packages
       /demo
         /example
           /src
	      /Example.php
	   /composer.json
```

**Windows**
```
 D:/
   laravel/
     packages/
       demo/
         example/
           src/
	      Example.php
	   composer.json
```

In the last step, you will see, how you can use your package.

----
<table width="100%">
  <tr>
    <th>
      <a href="composer.md">[ < Previous ] Update yor composer.json on laravel</a>
    </th>
    <th style="text-align: right">
      <a href="update.md">Installing/Using your package [ Next > ]</a>
    </th>
  </tr>
</div>
