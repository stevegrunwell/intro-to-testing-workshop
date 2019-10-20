### @group

Used to run tests of a similar nature, across suites & classes:

```php
/**
 * @test
 * @group API
 * @group Posts
 */
public function users_should_not_see_private_posts()
{
    // ...
}
```

```sh
$ phpunit --group=Posts
```
<!-- .element: class="fragment" -->

Note:

* The @group tag lets us group tests — no matter where they live — together
    - Really useful when different areas of the app need tested together
    - Completely user-defined, and test methods can belong to multiple groups
