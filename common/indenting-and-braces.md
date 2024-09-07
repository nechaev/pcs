# Indenting and braces

- Code MUST use 4 spaces for indenting, not tabs;
- Code MUST NOT be a hard limit on line length; the soft limit MUST be 120 characters; lines SHOULD be 80 characters or less;
- There MUST be one blank line before and after the namespace declaration, and there MUST be one blank line after the block of use declarations;
- Opening braces MUST go on the same line, and closing braces MUST go on the next line after the body;
- Opening parentheses for control structures MUST NOT have a space after them, and closing parentheses for control structures MUST NOT have a space before.

## Example

```php
<?php

namespace Vendor\Package;

use ExampleInterface;

class Example extends BaseExample implements ExampleInterface {
    public function baseMethod($a, $b): bool {
        if ($a === $b) {
            return true;
        }

        return false;
    }
}
```
