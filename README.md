AlphaSnow/Utils
===========
[![License](https://poser.pugx.org/alphasnow/php-utils/license)](https://packagist.org/packages/alphasnow/php-utils)
[![Latest Stable Version](https://poser.pugx.org/alphasnow/php-utils/v/stable)](https://packagist.org/packages/alphasnow/php-utils)
[![Total Downloads](https://poser.pugx.org/alphasnow/php-utils/downloads)](https://packagist.org/packages/alphasnow/php-utils)
[![tests](https://github.com/alphasnow/php-utils/actions/workflows/tests.yml/badge.svg?branch=main)](https://github.com/alphasnow/php-utils/actions/workflows/tests.yml)
[![Coverage Status](https://coveralls.io/repos/github/alphasnow/php-utils/badge.svg?branch=main)](https://coveralls.io/github/alphasnow/php-utils?branch=main)

## Requirement
- PHP >= 7.2

## Install
```bash
composer require alphasnow/utils
```

## Example
```php
use AlphaSnow\Utils\ListTree;
$list = [
    ['id' => 1, 'pid' => 0, 'name' => 'node1'],
    ['id' => 2, 'pid' => 1, 'name' => 'node2'],
    ['id' => 3, 'pid' => 2, 'name' => 'node3'],
];
$tree = ListTree::listToTree($list);
/*
[
    ['id' => 1, 'pid' => 0, 'name' => 'node1', '_child' => [
        ['id' => 2, 'pid' => 1, 'name' => 'node2', '_child' => [
            ['id' => 3, 'pid' => 2, 'name' => 'node3']
        ]]
    ]],
];
*/

$name = snake_name('ArticleCategory')
// article_category
```

## scripts
```bash
# composer exec --list

# Fix PHP code style
composer exec php-cs-fixer

# PHP Static Analysis
composer exec phpstan
```

## Credits

- [AlphaSnow][link-author]

## License
MIT License. See the [LICENSE](LICENSE.txt) file.


[link-author]: https://github.com/alphasnow
