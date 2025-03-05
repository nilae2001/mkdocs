# Integrating EJS with Express for Rendering Templates

## Installing EJS

Before using EJS in an Express project, install it as a dependency:

```sh
npm install ejs
```

## Setting Up Express to Use EJS
To configure Express to use EJS as the templating engine, set the view engine property:

```js
const express = require('express');
const app = express();

// Set EJS as the view engine
app.set('view engine', 'ejs');

// Define the directory for EJS templates (default is './views')
app.set('views', './views');

app.get('/', (req, res) => {
    res.render('index', { title: 'Home Page', message: 'Welcome to EJS with Express!' });
});

app.listen(3000, () => {
    console.log('Server is running on http://localhost:3000');
});
```

## Creating an EJS Template
Inside the views folder, create a file called index.ejs:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title><%= title %></title>
</head>
<body>
    <h1><%= message %></h1>
</body>
</html>
```


