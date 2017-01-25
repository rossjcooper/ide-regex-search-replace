# IDE Regex Search and Replace Cheatsheet

##Echo

Replaces instances of `<?= $variable ?>` with blade's `{{ $variable }}` template syntax.

**Search:** `\<\?\=(.*)\?\>`

**Replace:** `\{\{$1\}\}`

##Foreach

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

##Errors

This is more for me to swap outputting errors to use my custom @error() directive.

```php
 {{$errors->first('name')}}
```

for

```php
 @error('name')
```

**Search:** `\{\{ \$errors\-\>first\(\'(.*)\'\) \}\}`

**Replace:** `\@error\(\'$1\'\)`

