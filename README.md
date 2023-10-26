# Tutorial Install Express in Node.js

-   1. Create folder in PC

```bash
mkdir express
cd express
```

-   2. Create package.json

```bash
npm init -y
```

-   3. Install express

```bash
npm install express
```

-   4. install nodemon

```bash
# mac or linux
npm install --save-dev nodemon
# windows
npm install nodemon -g
```

-   5. Create index.js

```bash
const express = require('express');
const app = express();
app.get('/', (req, res) => {
    res.send('Hello World!');
});
app.listen(3000, () => {
    console.log('Example app listening on port 3000!');
});
```

-   6. Run index.js

```bash
node index.js
```

- 7. edit package.json

```bash
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "dev": "nodemon index.js"
  },
```
- 8. Install Prettier

```bash
npm install --save-dev --save-exact prettier
```
- 9. Create .prettierrc.json

```bash
touch .prettierrc.json
```

- 10. edit .prettierrc.json
```bash
{
    "tabWidth": 4,
    "singleQuote": true,
    "jsxSingleQuote": true,
    "semi": true,
    "printWidth": 150,
    "bracketSpacing": true,
    "braceSameLine": true
}
```

- 11. Run prettier
```bash
prettier --write .
```
- 12. edit package.json
```bash
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "dev": "nodemon index.js",
    "format": "prettier --write ."
  },
```
- 13. Run index.js
```bash
npx prettier --write . 
```

