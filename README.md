# This Package Uses Fetch

If you've landed here from a JavaScript package's documentation, it means that the aforementioned package uses [fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API) internally, and wants to help you polyfill it if needed.

For more information on why we created this document, visit LINK_TO_OUR_BLOG_POST

## Do I need a polyfill?

Here's a brief definition of a [polyfill](https://developer.mozilla.org/en-US/docs/Glossary/Polyfill):

> A polyfill is a piece of code (usually JavaScript on the Web) used to provide modern functionality on older environments that do not natively support it.


In the case of `fetch`, this will primarily be:

- Browsers: Opera Mini & IE
- Server: Node v17 or lower

## Polyfills

There are many polyfills out there, but here are the ones we'll recommend:

- node implementation: [node-fetch](https://github.com/bitinn/node-fetch)
- browser polyfill: [whatwg-fetch](https://github.com/github/fetch)

## Adding polyfills

To polyfill fetch in the global scope, you'll have to do the following in your application's entry point (or at least, before the package that needs fetch is imported):


- server:

```ts
import fetch from 'node-fetch';
global.fetch = fetch;
```

- browser:

```ts
// browser
import 'whatwg-fetch';
```
