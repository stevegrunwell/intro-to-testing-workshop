### Factories

<pre class="hljs lang-php"><code class="fragment">// A generic user object.
$user = factory(User::class)->make();</code>
<code class="fragment">// Set specific attributes.
$user = factory(User::class)->make([
    'email' => 'test@example.com',
]);</code>
<code class="fragment">// Persist the new model to the database.
$user = factory(User::class)->create();</code>
<code class="fragment">// Create + persist multiple entries (returns a Collection)
$users = factory(User::class, 3)->create();</code></pre>

Note:

Laravel factories let us easily generate data for our tests.

We define factories for our models, then can generate them at-will.

Remember: make() will hydrate the object, while create() will hydrate + persist it.
