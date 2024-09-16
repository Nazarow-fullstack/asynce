# Synchronous code
+ Synchronous means the code runs in a particular sequence of instructions given
in the program. Each instruction waits for the previous instruction to complete
its execution.
every line of code is executed one after the other, and each task must wait for the previous one to be completed before moving to the next

```javascript
 console.log("Hi");
 console.log("Geek");
 console.log("How are you?");
```

## Asynchronous
+ Asynchronous programming provides opportunities for a program to continue
running other code while waiting for a long-running task to complete. The timeconsuming task is executed in the background while the rest of the code continues to
execute
```javascript
function resolveAfter2Seconds() {
  return new Promise((resolve) => {
    setTimeout(() => {
      resolve('resolved');
    }, 2000);
  });
}

async function asyncCall() {
  console.log('calling');
  const result = await resolveAfter2Seconds();
  console.log(result);
  // Expected output: "resolved"
}

asyncCall();
```
![](https://www.freecodecamp.org/news/content/images/2021/09/freeCodeCamp-Cover-2.png)

## we have three method with asynchronous
+ callback
```javascript
setTimeout(() => {
console.log('finish homework')
}, 500);
console.log('start homework'
```

+Promise
```javascript
const promise1 = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve('foo');
  }, 300);
});

promise1.then((value) => {
  console.log(value);
  // Expected output: "foo"
});

console.log(promise1);
// Expected output: [object Promise]
```
+ async/await
```javascript
async function f() {
  return 1;
}

f().then(alert);
```
