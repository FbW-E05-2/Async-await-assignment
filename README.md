## Async await assignments

###  Assignment 1 
We have a “regular” function called `getResult`. How can you call the `async` function `wait()` and use its result inside of `getResult`?

```javascript
async function wait() {
  await new Promise(resolve => setTimeout(resolve, 3000));

  return 'Hello World';
}

function getResult() {
  // ...what should you write here?
  // we need to call async wait() and wait to get Hello World
  // remember, we can't use "await"
 
 wait().then(result => alert(result));
 
}
getResult()
```

### Assignment 2 
```js
function randomImg() {
  return new Promise(resolve => {
    setTimeout(() => {
      resolve('https://picsum.photos/200/300?random=1');
    }, 2000);
  });
}

async function getImg() {
  // ...what should you write here?
  // we need to call randomImg() and wait to get the image
  // you need to use "await"
  // you need to put the image inside the body 
}

getImg(); // image inside the body   <-- after 2 seconds
```



