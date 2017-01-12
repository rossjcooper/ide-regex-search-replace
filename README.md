# IDE Regex Search and Replace Cheatsheet

##PHP Shorthand Echo to Blade Echo
Replaces instances of `<?= $variable ?>` with blade's `{{ $variable }}` template syntax.

**Search:** `\<\?\=(.*)\?\>`

**Replace:** `\{\{$1\}\}`

##PHP Foreach to Blade Foreach
Replaces typical foreach blocks
```php
 <?php foreach($list as $item): ?>
 //...	
 <?php endforeach; ?>
```

for


```php
@foreach($list as $item)
 //...
@endforeach
 
```

**Search:** `\<\?php foreach\((.*)\): \?\>`

**Replace:** `\@foreach\($1\)`

**Search:** `\<\?php endforeach\; \?\>`

**Replace** `\@endforeach`
