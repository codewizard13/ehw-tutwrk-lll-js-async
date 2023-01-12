# COURSE: JavaScript: Async (2021)

---

NOTES:

---

- Restaurants work on an asynchronous model. Many people can be doing different things with minimal blocking.

--

- 2 different program flows: Synchronus and Asynchronous

- Synchronous Program Flow
  - One statement at a time
  - Statements executed in order
  - Blocking
  - Can needlessly slow down our program flow
  - Later statements aren't executed until after a previous statement is finished


- Asynchronous Program Flow
  - AKA: async
  - Parser can start executing some code and continue that execution while other code is executed as well
  - Technically JS has only single thread, but it does have parallel process execution
  - multiple statements at once
  - simultaneous execution
  - non blocking

- We write async code when want to give part of our code time to complete while still allowing the parser to continue executing the code that follows right away

- Most common use case: AJAX requests
- XHR, fetch or library method that sends a request for data to a remote server
- defaults to async mode

- Set Timer: timer can run while program then executes rest of the code


---

## Built-in Async JavaScript Features

- XMLHttpRequest methods
- setTimeout()
- requestAnimationFrame(), and more

## Callback Pattern

- async func called, executed in parallel while main program flow continues
- takes another function as an argument
- after statements of original function, function passed as arg is called (callback function)

### Callback Function:

- specifies what should happen next after function is executed async

### setTimeous() Example

- 2 args: callback function and delay time in ms
- common to specify anonymous function as the callback

```js

// First delay for 5secs, then print "Hello world" to console
setTimeout(function() {
  console.log('Hello world')
}, 5000)
```