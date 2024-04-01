# PHP Coding Standard

## Motivation

The goal of this document is to summarize the rules for PHP code based on:

1. Interfaces that the language provides
2. Common sense
3. Ease of use

## How to read

The CAPITALIZED words throughout these standard have a special meaning:

> ```text
> The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT",
> "SHOULD", "SHOULD NOT", "RECOMMENDED",  "MAY", and "OPTIONAL" in 
> this document are to be interpreted as described in RFC2119.
> ```

Refer to [RFC2119](https://www.ietf.org/rfc/rfc2119) for details.

## Code example

```php
<?php declare(strict_types=1);

namespace Vendor\Package;

use Vendor\Package\{ClassA as A, ClassB, ClassC as C};
use Vendor\Package\SomeNamespace\ClassD as D;

use function Vendor\Package\{functionA, functionB, functionC};

use const Vendor\Package\{ConstantA, ConstantB, ConstantC};

class ExampleClass extends SpecificClass implements ExampleInterface {
    public const TYPE_HIDDEN  = 0;
    public const TYPE_VISIBLE = 10;
    /** Explain text for constant */
    public const TYPE_TRANSPARENT = 100;

    public    ?string $maybe_string = null;
    protected int     $count        = 0;

    public static int $static_property = 0;

    public function exampleFunction(int $a, int $b = null): array {
        if (
            $long_expression1
            && $long_expression2
        ) {
            // Do something
        } elseif ($short_expression) {
            // Do something another
        } else {
            // Do default things
        }

        return [];
    }

    /**
     * @param Gift[] $wishlist
     */
    public function aVeryLongMethodName(
        Person $very_important_person,
        int $full_age,
        array $wishlist = [],
    ): string {
        // Method body
    }

    final public static function getBar(): Bar {
        // Method body
    }
}

class ClassName extends ParentClass implements
    \ArrayAccess,
    \Countable,
    \Serializable
{
    // Constants, properties, methods
}
```
