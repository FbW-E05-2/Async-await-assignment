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



## Assignment 3

- We have a “regular” function called `run` and “async” function called “catchFunction” . How can you call the 
`async` function `getOffers()` using `try catch` to use its result inside of `run`?
- replace the return inside getOffer with : 

```js
return Promise.resolve( 'the are 10 offers 😀  ');

```

> `Promise.resolve()` and `Promise.reject()` are another way to resolve and reject the promise

```js
 async function getOffers() {
   return Promise.reject( new Error('sorry we have an error connecting to the server! '))
  
  
 }
 
 async function catchFunction() {
     try { 
       // here you need to call getOffers using await 
       // you need to return the value of calling getOffers
        
     } catch (err) {
        // here you need to log the error message
         
     }
     return 'no data found 😑'
         
  
 }
 
 async function run() {
     const value = await catchFunction();
     console.log(value);
 }
 
 run();
```