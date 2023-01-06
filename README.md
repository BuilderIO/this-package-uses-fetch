# This Package Uses Fetch

If you've landed here from a JavaScript package's documentation, it means that the aforementioned package uses [fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API) internally, and wants you to know about it.

For more information on why we created this document, visit LINK_TO_OUR_BLOG_POST

## Do I need a polyfill?

TBD: show overall support chart? 

- browser: opera mini & IE
- server: node v17 or lower

## Polyfills

For environments that don't support fetch, you'll need to provide polyfills of your choosing. Here are the ones we recommend:

- node implementation: [node-fetch](https://github.com/bitinn/node-fetch)
- browser polyfill: [whatwg-fetch](https://github.com/github/fetch)

#### Adding polyfills

This means that you can set the polyfills in the global scope:

```ts
// server
import fetch from 'node-fetch';
global.fetch = fetch;

// browser
import 'whatwg-fetch';
```
