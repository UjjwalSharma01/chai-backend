## taking app to production 
- Create a `.env` file in the root directory of the project.
- Add the following code in the `.env` file.
```env
PORT=4000 // everything here stays in caps in general
```
- Add the following code in the `index.js` file.
```javascript
require('dotenv').config(); // this will load the environment variables from the .env file
const express = require('express');
const app = express();
app.get('/', (req, res) => {
  res.send('Hello World!');
});

// bacha kucha code
app.listen(process.env.PORT, () => {
  console.log(`Example app listening at http://localhost:${process.env.PORT}`);
});
```