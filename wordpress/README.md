# WordPress
Easy deployment container for WordPress.

## Tip
Dont forget to add the following line to your ```wp-config.php```

```php
/* Make WordPress install plugins directly */
define('FS_METHOD', 'direct');
```

Also, to make the root directory files writable from outsite the container, run the following command in that folder:
```bash
$ sudo chmod -R a+rw ./*
```