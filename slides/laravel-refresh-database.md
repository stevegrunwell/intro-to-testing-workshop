### Refresh database

```php
use Illuminate\Foundation\Testing\RefreshDatabase;
use Tests\TestCase;

class MyTestClass extends TestCase
{
    use RefreshDatabase;

    // ...
}
```

Note:

The RefreshDatabase trait will automatically clear out the test database between each test method

Uses the fixtures (setUp/tearDown) we discussed earlier
