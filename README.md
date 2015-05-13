# lumen-doctrine

Doctrine module for the Lumen PHP framework.

## Requirements

- PHP >= 5.5

## Usage

### Install through Composer

Run the following command to install the package:

```sh
composer require nordsoftware/lumen-doctrine
```

### Register the Service Provider

Add the following line to ```bootstrap/app.php```:

```php
$app->register('Nord\Lumen\Doctrine\DoctrineServiceProvider');
```

You can now use the ```EntityManager``` facade or inject the ```EntityManagerInterface``` where needed.

### Configure

Copy ```config/doctrine.php``` into ```config``` and modify it if necessary.

The available configurations are:

- **mapping** - Mapping driver to use (xml, yaml or annotations), defaults to xml
- **paths** - Paths to entity mappings, defaults to an empty array
- **types** - Custom Doctrine types to register, defaults to an empty array
- **proxy** - Proxy configuration
- **repository** - Repository class to use
- **logger** - Logger class to use

### Run Artisan

Run ```php artisan``` and you should see the new commands in the doctrine:* namespace section.

## Contributing

Contributions are most welcome. Please note the following guidelines before submitting pull requests:

- Format code according to the [PSR standards](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md)

## License

See [LICENSE](LICENSE).