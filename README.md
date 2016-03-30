<a href="https://promisesaplus.com/">
    <img src="https://promisesaplus.com/assets/logo-small.png" alt="Promises/A+ logo" align="right" />
</a>

# Awesome Promises [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

> A curated list of useful resources for JavaScript Promises

Inspired by the [awesome](https://github.com/sindresorhus/awesome) list thing. Not to be confused with other awesome promises like "I promise you a million dollars" or "I promise you'll stay fit and never have to go to the gym again".

**Table of Contents**

- [Resources, Blogs, and Books](#resources-blogs-and-books)
- [Promises/A+ Implementations (ES6/ES2015 compatible)](#promisesa-implementations-es6es2015-compatible)
  - [Strict Implementations](#strict-implementations)
  - [Implementations with extras](#implementations-with-extras)
  - [Fallbacks](#fallbacks)
- [Convenience Utilities](#convenience-utilities)

## Resources, Blogs, and Books

### For beginners
* [Promise Cookbook](https://github.com/mattdesl/promise-cookbook) - The why, what, and how. "A brief introduction [...] primarily aimed at frontend developers".
* [Promises for Asynchronous Programming](http://exploringjs.com/es6/ch_promises.html) - Chapter from [Exploring ES6](http://exploringjs.com/)
* [You Don't Know JS: Promises](https://github.com/getify/You-Dont-Know-JS/blob/master/async%20&%20performance/ch3.md) - Chapter from [You Don't Know JS: Async & Performance](https://github.com/getify/You-Dont-Know-JS/tree/master/async%20%26%20performance)
* [JavaScript Promises: There and back again](http://www.html5rocks.com/en/tutorials/es6/promises/) - Basics of JavaScript's native promise implementation.
* [JavaScript with Promises](http://shop.oreilly.com/product/0636920032151.do) - from O'Reilly. Short and to-the-point. Uses native and bluebird.
* [Promise it won't hurt](https://github.com/stevekane/promise-it-wont-hurt) - An interactive [nodeschool](http://nodeschool.io/) workshop
* [ES6 Kata Promises](http://es6katas.org/) - Promises Katas : [Basics](http://tddbin.com/#?kata=es6/language/promise/basics)
* [ES6 Promises in Depth](https://ponyfoo.com/articles/es6-promises-in-depth)

### Deep Dive
* [You're Missing the Point of Promises](https://blog.domenic.me/youre-missing-the-point-of-promises/) - Promises are much more than callback aggregation, and that jQuery's implementation (prior to 3.0) isn't enough.
* [We have a problem with promises](https://pouchdb.com/2015/05/18/we-have-a-problem-with-promises.html) - "Many of us are using promises without really understanding them."
* [Promise anti-patterns](https://github.com/petkaantonov/bluebird/wiki/Promise-anti-patterns) - Common misuses and how to avoid them.
* [Promise anti-patterns (2)](http://taoofcode.net/promise-anti-patterns/) - Another set of promises anti-patterns
* [Promise Ponderings, (Anti-)Patterns, and Apologies](https://sdgluck.github.io/2015/08/24/promise-ponderings-patterns-apologies/) - Promise behaviour demonstrated and explained by common questions and their answers.
* [Javascript Promises...In Wicked Detail](http://www.mattgreer.org/articles/promises-in-wicked-detail/) - Recreate the promise implementation
* [Writing Promise-Using Specifications](https://www.w3.org/2001/tag/doc/promises-guide) - "This document gives guidance on how to write specifications that create, accept, or manipulate promises"

### References
* [Promises/A+ specification](https://promisesaplus.com/)
* [caniuse promises](http://caniuse.com/#feat=promises)
* [Fates and States](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md) - Quick definitions of possible states.
* [Promisees](https://bevacqua.github.io/promisees/) - Promise visualization playground for the adventurous.

## Promises/A+ Implementations (ES6/ES2015 compatible)

### Strict Implementations
These implement no more or less than the es6 spec. They make great polyfills and are exceptionally compatible with native promises.

* [pinkie](https://github.com/floatdrop/pinkie) - Ponyfill. Node-oriented, but [browserifyable](https://github.com/substack/node-browserify). *Extremely* small implementation.
* [native-promise-only](https://github.com/getify/native-promise-only) - Polyfill. Browser and node-compatible.
* [es6-promise](https://github.com/stefanpenner/es6-promise) - Opt-in polyfill. A strict-spec subset of rsvp.js.
* [lie](https://github.com/calvinmetcalf/lie) - Small, browserifyable with an opt-in polyfill.

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

* [pify](https://github.com/sindresorhus/pify) - Promisify ("denodify") a callback-style function.
* [promise-each](https://github.com/yoshuawuyts/promise-each) - Standalone `bluebird.each`. Execute one after the other sequentially.
* [promise-filter](https://github.com/yoshuawuyts/promise-filter) - Standalone `bluebird.filter`. Filter an array to a promise.
* [promise-finally](https://github.com/blakeembrey/promise-finally) - Standalone bluebird `finally()`. Execute a handler unconditionally after others have been handled.
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
* [lie-fs](https://www.npmjs.com/package/lie-fs) - Promise wrappers for Node's FS API.
* [immediate-promise](https://github.com/sindresorhus/immediate-promise) - Returns a promise resolved in the next event loop - think `setImmediate()`.
* [delay](https://github.com/sindresorhus/delay) - Delay a promise a specified amount of time.
* [promise-whilst](https://github.com/sindresorhus/promise-whilst) - Calls a function repeatedly if and while a condition returns true and then resolves the promise.
* [loud-rejection](https://github.com/sindresorhus/loud-rejection) - Make unhandled promise rejections fail loudly instead of the default silent fail.
* [promise-until](https://github.com/busterc/promise-until) - Calls a function repeatedly if a condition returns false and until the condition returns true and then resolves the promise.
* [promise-do-until](https://github.com/busterc/promise-do-until) - Calls a function repeatedly until a condition returns true and then resolves the promise.
* [promise-do-whilst](https://github.com/busterc/promise-do-whilst) - Calls a function repeatedly while a condition returns true and then resolves the promise.
* [promise-semaphore](https://github.com/samccone/promise-semaphore) - Push a set of work to be done in a configurable serial fashion

## License
Licensed under the [Creative Commons CC0 License](https://creativecommons.org/publicdomain/zero/1.0/).
