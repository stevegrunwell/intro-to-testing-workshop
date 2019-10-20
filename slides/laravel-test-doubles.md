### Mocking with Laravel

```php
use App\Services\SomeService;
use Mockery;

$mock = Mockery::mock(SomeService::class);
$mock->shouldReceive('someMethod')
    ->once()
    ->with('arg1', 'arg2');

// Bind our mock to the SomeService service.
$this->instance(SomeService::class, $mock);
```

Note:

Thanks to Laravel's service container, we can inject Mockery instances for testing
