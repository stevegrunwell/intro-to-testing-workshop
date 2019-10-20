### Test Classes

```php
<?php

namespace Tests;

use Illuminate\Foundation\Testing\TestCase as BaseTestCase;

abstract class TestCase extends BaseTestCase
{
    use CreatesApplication;
}
```

Note:

* Laravel gives us our own test class by default
* CreatesApplication trait handles setting up the Laravel environment
