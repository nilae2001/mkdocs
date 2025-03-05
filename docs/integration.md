# Integrating EJS with Express for Rendering Templates

## Overview

**EJS (Embedded JavaScript)** is a templating engine that allows dynamic content rendering in Express applications. This documentation provides step-by-step instructions on setting up **Express** to use **EJS for** rendering templates. It covers configuring **Express**, setting the view engine, and rendering templates from routes.

## Installing EJS

Before using **EJS** in an **Express** project, install it as a dependency:

```sh
npm install express
```

## Configuring Express to Use EJS 
Before rendering templates, Express must be configured to recognize EJS as the templating engine.

## Steps
1. **Import Express**: Require the Express module in your application file.
    ```js
    const express = require('express');
    ```

2. **Initialize the Express Spp**: Create an instance of an Express application.
    ```js
    const app = express();
    ```

3. **Set EJS as the View Engine**: Configure Express to use EJS for rendering templates.
    ```js
    app.set('view engine', 'ejs');
    ```

4. **Set the Views Directory**: Define the folder where EJS templates will be stored.
    ```js
    app.set('views', __dirname + '/views');
    ```

!!! note 
    The default directory for views is ```./views```. If templates are in a different location, update path accordingly.

## Rendering an EJS Template from an Express Route
Once **EJS** is configured, Express routes must be set up to render templates dynamically.

## Steps
1. **Create an Express Route**: Define a route that will render an EJS template.
    ```js
    app.get('/', (req, res) => {
        res.render('index');
    });
    ```

2. **Create the Template File**: Inside the ```views``` directory, create ```index.ejs```.
    ```html
    <!DOCTYPE html>
    <html>
    <head>
        <title>Home Page</title>
    </head>
    <body>
        <h1>Welcome to the Home Page</h1>
    </body>
    </html>
    ```

3. **Start the Express Server**: Run the server to test the template rendering.
    ```js
    app.listen(3000, () => {
        console.log('Server is running on http://localhost:3000');
    });
    ```

4. **Verify in Browser**: Open ```http://localhost:300``` in a browser to check if the template renders correctly

!!! warning
    If ```res.render()``` fails with an error, verify that EJS is installed (```npm install ejs```) and that the views directory exists.

# Conclusion
With this configuration, Express successfully renders EJS templates from routes, allowing dynamic page content to be served.