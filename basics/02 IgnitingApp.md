## Hello world program in express
```javascript
const express = require('express');
const app = express();
const port = 3000;
// using get method to get to listen to the request and giving callback function to send the response.
app.get('/', (req, res) => {
  res.send('Hello World!');
});
// don't forget to add '/' 
app.get('/twitter',(req, res)=>{
    res.send("ujjwalsharma01")
})

app.listen(port, () => {
  console.log(`Example app listening at http://localhost:${port}`);
});
```

if you run save this code and run the command
```bash
node index.js
```
and if you go to url `http://localhost:3000/` you will se the output as `Hello World!` and if you go to url `http://localhost:3000/twitter` you will see the output as `ujjwalsharma01`

but when the app is running if you make any changes in the code then you have to stop the server and run the server again. to avoid this we can use nodemon. nodemon is a package that will automatically restart the server when you make any changes in the code.

## taking app to production
you can't take the app directly to the production because currently we are using port 3000 as mandatory. but in production we can't use the port 3000 because there might be a possibility that the given port is not free in that service at that time. so we have to use the environment variable to get the port number.

__installing env__
```bash
npm i dotenv
```

for further steps refer to the next chapter. [Igniting App](./02%20IgnitingApp.md)