### More Test Doubles

<pre class="hljs fragment-replacement"><code class="lang-php">use Illuminate\Support\Facades\Event;

</code><code class="lang-php fragment fade-out" data-fragment-index="0">Event::fake();
</code><code class="lang-php fragment fade-in" data-fragment-index="0">Event::fake([
    PostCreated::class,
]);</code></pre>


Note:

Most of Laravel's facades have built-in support for Mockery.

Using the Facade's ::fake() method tells Laravel to swap it out for a Mockery instance. This prevents things that may be hooked into it from firing.

If we only want to prevent some events, we can typically pass an array of things we want to fake and let everything else operate normally.
