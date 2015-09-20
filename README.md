<a href="http://promisesaplus.com/">
    <img src="http://promisesaplus.com/assets/logo-small.png" alt="Promises/A+ logo" align="right" />
</a>

# Awesome Promises [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

> A curated list of useful resources for JavaScript Promises

Inspired by the [awesome](https://github.com/sindresorhus/awesome) list thing. Not to be confused with other awesome promises like "I promise you a million dollars" or "I promise you'll stay fit and never have to go to the gym again".

## Resources, Blogs, and Books

* [caniuse promises](http://caniuse.com/#feat=promises)
* [Promise Cookbook](https://github.com/mattdesl/promise-cookbook) The why, what, and how. "A brief introduction [...] primarily aimed at frontend developers".
* [You're Missing the Point of Promises](https://blog.domenic.me/youre-missing-the-point-of-promises/) @domenic shows that promises are much more than callback aggregation, and that jQuery's implementation (prior to 3.0) isn't enough.
* [JavaScript Promises: There and back again](http://www.html5rocks.com/en/tutorials/es6/promises/) Basics of JavaScript's native promise implementation.
* [Fates and States](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md) Quick definitions of possible states.
* [Promise anti-patterns](https://github.com/petkaantonov/bluebird/wiki/Promise-anti-patterns) Common misuses and how to avoid them.
* [JavaScript with Promises](http://shop.oreilly.com/product/0636920032151.do) from O'Reilly. Short and to-the-point. Uses native and bluebird.
 * [We have a problem with promises](http://pouchdb.com/2015/05/18/we-have-a-problem-with-promises.html) Are you a promise expert ?
 
## Promises/A+ Implementations (ES6/ES2015 compatible)

### Strict Implementations
These implement no more or less than the es6 spec. They make great polyfills and are exceptionally compatible with native promises.

* [pinkie](https://github.com/floatdrop/pinkie) Ponyfill. Node-oriented, but [browserifyable](https://github.com/substack/node-browserify). *Extremely* small implementation.
* [native-promise-only](https://github.com/getify/native-promise-only) Polyfill. Browser and node-compatible.
* [es6-promise](https://github.com/jakearchibald/es6-promise) Opt-in polyfill. A strict-spec subset of rsvp.js.

### Implementations with extras
All of these provide more features than the language yet remain compatible. Node + Browsers for all.

* [bluebird](https://github.com/petkaantonov/bluebird) - Fully featured, extremely performant. Long stack traces & generator/coroutine support.
* [rsvp.js](https://github.com/tildeio/rsvp.js/) - Lightweight with a few extras. Compatible down to IE6!
* [Q](https://github.com/kriskowal/q) - One of the original implementations. Long stack traces and other goodies.
* [then/promise](https://github.com/then/promise) - Small with `nodeify`, `denodify` and `done()` additions.
* [when.js](https://github.com/cujojs/when) - Packed with control flow, functional, and utility methods.


### Fallbacks
* [native-or-bluebird](https://www.npmjs.com/package/native-or-bluebird) - Helps transition to completely native.
* [pinkie-promise](https://github.com/floatdrop/pinkie-promise) - Use native, or fall back to `pinkie`. Great for node library authors.
* [any-promise](https://github.com/kevinbeaty/any-promise) - Loads the first available implementation. Safe for browserify.

## Convenience Utilities
Native and strictly spec-compliant promises are awesome for compatibility, future-proofness, library authors, and browsers. However, libraries like bluebird patch goodies onto the `Promise` constructor and prototype. Solution? tiny modules of course!

* [pify](https://github.com/sindresorhus/pify) - Promisify ("denofify") a callback-style function.
* [promise-every](https://github.com/yoshuawuyts/promise-each) - Standalone `bluebird.every`. Execute one after the other sequentially.
* [promise-filter](https://github.com/yoshuawuyts/promise-filter) - Standalone `bluebird.filter`. Filter an array to a promise.
* [promise-map](https://github.com/yoshuawuyts/promise-map) - Standalone `bluebird.map`. Map an array to a promise.
* [promise-method](https://github.com/wbinnssmith/promise-method) - Standalone `bluebird.method`. Turn a synchronously-returning method into a promise-returning one.
* [promise-props](https://github.com/exponentjs/promise-props) - Standalone implementation of bluebird's `bluebird.props` or rsvp's `RSVP.hash`
* [promise-reduce](https://github.com/yoshuawuyts/promise-reduce) - Standalone `bluebird.reduce`. Reduce an array to a promise.
* [promise-some](https://github.com/yoshuawuyts/promise-some) - Standalone `bluebird.some`. Check if an element passes the predicate, return a promise.
* [promise-try](https://github.com/wbinnssmith/promise-try) - Standalone `bluebird.try`. Execute a synchronously-returning function and return a promise.

* [is-promise](https://github.com/then/is-promise) - Determine if something looks like a Promise.
* [sprom](https://github.com/then/sprom) - Resolve when a stream ends. Optional buffering (be careful with this!)

* [task.js](https://github.com/mozilla/task.js) - Write async functions in a blocking style using promises and generators. Like `bluebird.coroutine`.
* [co](https://github.com/tj/co) - Like `task.js` and `bluebird.coroutine`, but supports thunks too.
