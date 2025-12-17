SensioFrameworkExtraBundle
==========================

This bundle provides a way to configure your controllers with annotations and PHP attributes.

**Note**: This bundle is maintained for backward compatibility. For new projects, consider using native PHP attributes as added in Symfony core.
For full support, use [Symfony 6.2+](https://symfony.com/blog/new-in-symfony-6-2-built-in-cache-security-template-and-doctrine-attributes).

## Features

- **Annotations Support**: Configure controllers using Doctrine annotations
- **PHP Attributes Support**: Configure controllers using PHP 8.0+ attributes
- **Symfony 7 Compatibility**: Full compatibility with Symfony 7.0+

## Usage

### Annotations (Legacy)
```php
use Sensio\Bundle\FrameworkExtraBundle\Configuration\Template;
use Sensio\Bundle\FrameworkExtraBundle\Configuration\IsGranted;

/**
 * @Template("default/index.html.twig")
 * @IsGranted("ROLE_USER")
 */
public function index()
{
    // ...
}
```

### PHP Attributes (Recommended)
```php
use Sensio\Bundle\FrameworkExtraBundle\Configuration\Template;
use Sensio\Bundle\FrameworkExtraBundle\Configuration\IsGranted;

#[Template('default/index.html.twig')]
#[IsGranted('ROLE_USER')]
public function index()
{
    // ...
}
```

Read about it on its [official homepage](http://symfony.com/doc/current/bundles/SensioFrameworkExtraBundle/index.html).
