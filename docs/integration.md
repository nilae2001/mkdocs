# Integrating EJS with Express for Rendering Templates

## Overview

**EJS (Embedded JavaScript)** is a templating engine that allows dynamic content rendering in Express applications. 

This documentation provides step-by-step instructions on setting up **Express** to use **EJS for** rendering templates. It covers configuring **Express**, setting the view engine, and rendering templates from routes.

## Installing EJS

Before using **EJS** in an **Express** project, install it as a dependency:

```sh
npm install express
```

## Configuring Express to Use EJS 
Before rendering templates, Express must be configured to recognize EJS as the templating engine.

### 1. **Import Express**: Require the Express module in your application file.
    ```js
    const express = require('express');
    ```

### 2. **Initialize the Express Spp**: Create an instance of an Express application.
    ```js
    const app = express();
    ```

### 3. **Set EJS as the View Engine**: Configure Express to use EJS for rendering templates.
    ```js
    app.set('view engine', 'ejs');
    ```

### 4. **Set the Views Directory**: Define the folder where EJS templates will be stored.
    ```js
    app.set('views', __dirname + '/views');
    ```

!!! note 
    The default directory for views is ```./views```. If templates are in a different location, update path accordingly.

## Rendering an EJS Template from an Express Route
Once **EJS** is configured, Express routes must be set up to render templates dynamically.

### 1. **Create an Express Route**: Define a route that will render an EJS template.
    ```js
    app.get('/', (req, res) => {
        res.render('index', { name: 'John Doe', userLoggedIn: true });
    });
    ```
    When you pass data to the **EJS** template using ```res.render()```, the data is sent as an object. In this case, we are passing two properties: ```name``` and ```userLoggedIn```. These properties become available in the **EJS** template, where we can dynamically insert them into the HTML. For example, the ```name``` property can be used to personalize the message, and the ```userLoggedIn``` property controls which content is shown based on the user's login status. 
    
    This process allows you to inject dynamic, context-specific information into your views directly from your Express route handlers.

### 2. **Create the Template File**: Inside the ```views``` directory, create ```index.ejs```.
    ```html
    <html>
       <body>
         <% if (userLoggedIn) { %>
           <h1>Welcome back, <%= name %>!</h1>
         <% } else { %>
           <h1>Please log in</h1>
         <% } %>
       </body>
     </html>
    ```
    This will render the "Welcome back, John Doe!" message if `userLoggedIn` is `true`.

### 3. **Start the Express Server**: Run the server to test the template rendering.
    ```js
    app.listen(3000, () => {
        console.log('Server is running on http://localhost:3000');
    });
    ```

### 4. **Verify in Browser**: Open ```http://localhost:300``` in a browser to check if the template renders correctly
![Welcome back, John screenshot](images/localhost3000.png)

!!! warning
    If ```res.render()``` fails with an error, verify that EJS is installed (```npm install ejs```) and that the views directory exists.

# Conclusion
With this configuration, Express successfully renders EJS templates from routes, allowing dynamic page content to be served.