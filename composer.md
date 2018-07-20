# Update yor composer.json on laravel

Now, you had created  your `packages` directory - Here you will create later your own laravel packages.

In your laravel project, you find the file `composer.json` - here you must add some configuration to find your local packages. Open the file and add following entries:

**Linux:** `/opt/laravel/composer.json` 
```json
{
    // ...
    
    "repositories": [
        {
            "type": "path",
            "url": "/opt/laravel/packages",
            "options": {
                "symlink": true
            }
        }
    ]
}
```

**Windows:** `D:/laravel/composer.json` 
```json
{
    // ...
    
    "repositories": [
        {
            "type": "path",
            "url": "D:/laravel/packages",
            "options": {
                "symlink": true
            }
        }
    ]
}
```

That's is it!

----
<table width="100%">
  <tr>
    <th>
      <a href="environment.md">[ < Previous ] Create yor local package environment</a>
    </th>
    <th style="text-align: right">
      <a href="create.md">Create your first package [ Next > ]</a>
    </th>
  </tr>
</div>
