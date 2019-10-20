### HTTP Requests

```php
public function demonstrate_http_requests()
{
    // A simple GET request.
    $this->get('/');

    // Make an authenticated POST request to a named route.
    $this->actingAs(factory(User::class)->create())
        ->post(route('posts.store'), [
            'content' => 'Some post content',
        ]);
}
```

Note:

The Illuminate\Foundation\Testing\Concerns\MakesHttpRequests trait enables us to emulate HTTP requests to the Laravel application

Very useful in integration tests, letting you "black box" the request.

You provide the request, then analyze the response.
