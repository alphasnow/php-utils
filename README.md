AlphaSnow/Utils
===========

[![Latest Stable Version](https://poser.pugx.org/alphasnow/utils/v/stable)](https://packagist.org/packages/alphasnow/utils)
[![Total Downloads](https://poser.pugx.org/alphasnow/utils/downloads)](https://packagist.org/packages/alphasnow/utils)
[![tests](https://github.com/alphasnow/php-utils/actions/workflows/tests.yml/badge.svg)](https://github.com/alphasnow/php-utils/actions/workflows/tests.yml)
[![Coverage Status](https://coveralls.io/repos/github/alphasnow/php-utils/badge.svg?branch=0.x)](https://coveralls.io/repos/github/alphasnow/php-utils/badge.svg?branch=0.x)

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

## Credits

- [AlphaSnow][link-author]

## License
MIT License. See the [LICENSE](LICENSE) file.



[link-author]: https://github.com/alphasnow
