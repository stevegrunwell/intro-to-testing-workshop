### Laravel Assertions

```php
/**
 * @test
 */
public function a_logged_in_user_is_shown_their_timeline()
{
    $this->actingAs(factory(User::class)->create())
        ->get(route('home'))
        ->assertSuccessful()
        ->assertViewIs('timeline');
}
```

Note:

Laravel ships with some built-in assertions as well

Built around HTTP response codes, URLs, views, session contents, etc.
