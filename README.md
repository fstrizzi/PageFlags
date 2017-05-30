# Page Flags

Simple API for flag pages. It differentiates between users and guests.

### Flag API

```php
$page->flag->save();	// flags the current page
```

Extended:

```php
$page->flag->comment = 'Your comment';
$page->flag->tags = array('like', 'favorite');
$page->flag->save();
```

You can remove the flag using `$page->flag->delete()`.

### User Flags API

You can get all flags of the user this way:

```php
$user->flags; //Returns an array all flags
```

```php
$user->flags(true); //Returns grouped by tag.
```

```php
$page->flag->tags //Returns all flags
```
```php
$page->flag->countFlagByPage(pageId); //Returns array with all tags and count
```

```php
$page->allFlagsByPage(pageId, listUsers); //Returns all page flags with their users.
```