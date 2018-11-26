## Progress Check 2
- [ ] Fork and clone this repo
- [ ] Write a working implementation of passwordProtect in `passwordProtect.js`
- [ ] Push your work to your fork

## passwordProtect
`passwordProtect(func, password)`

passwordProtect returns a function that, when called, only invokes func when the matching password is supplied as the first argument. When the matching password is supplied, any additional arguments should be passed to func and the return value of func should be returned from the created function. If the password does not match, func is not invoked and nothing is returned.

```javascript
var myFunc = function(a, b) {
  console.log('my func ran');
  return a + b;
};

var protectedMyFunc = passwordProtect(myFunc, 'p@ssw0rd');
protectedMyFunc('password', 1, 2); // nothing logged, nothing returned
protectedMyFunc('p@ssw0rd', 1, 2); // logs 'my func ran', returns 3
protectedMyFunc('p@ssw0rd', 13, 5); // logs 'my func ran', returns 18
```

## Allowed Resources
- [MDN](https://developer.mozilla.org/en-US/)
- [Chai](http://www.chaijs.com/api/bdd/)
- [Mocha](https://mochajs.org/)
