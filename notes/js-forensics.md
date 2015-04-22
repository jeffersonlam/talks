# JavaScript Forensics
Todd Gardner (TrackJS)  
@toddhgardner  
12:00pm–12:30pm Wednesday, 04/22/2015  
Pure Code and JavaScript  

## Notes
"I see the common problems just about every webapp runs into."
The 6 most common JS errors I come across in my everyday work.
##### `Script error.`
* Add `crossorigin="anonymous" into script-tags so the browser won't obfuscate errors coming from those files.
* `Script Error "Line 1"`

##### `Cannot read property of undefined`
* > "If I ever don't know what's going on, it's probably function hoisting."
* Third-Party Errors
    * Testing locally is no longer adequate. You have to understand what's going on in the production environment.

##### 'Cannot read property 'destroy' of undefined`
* Look at the stack trace. (anonymous function). Great. But Chrome dev tools can do more. Check off the `Async` button in the callstack, and we can see more.
* It's a `this` in a `setTimeout`. Immediate code smell.
* Use `.bind(this)` to keep the scope of `this` the same within the new function.
**Culprit: `Context "this" error`**

##### `undefined is not a function`
* Dig into the stack trace, with `async` stack traces on.
* We see some type-checking errors going on.
* Use `console.warn()` to show error messages.
**Culprit: `"Dirty" Data Error`**

##### `x is undefined`
**Culprit: `Loading "The EDGE" Error`**

##### Crashing Browser
* Use recorder to document node, listeners, documents being used. You can use `WASD` to navigate it!
* We can see all the increases in memory usage by the individual functions.
**Culprit: "Leaky" Memory Error**

"We need some way to handle the user experience of [bugs]."

## Action Items
* [ ] Start utilizing chrome dev tools, and practice debug-friendly coding
  * [ ] Start using `async` stack traces in Chrome dev tools.
  * [ ] Include debugging/error catching with warning messages when developing in JS.
  * [ ] Use the recording functionality.
