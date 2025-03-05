# Integrating EJS with Express for Rendering Templates

## Overview

**EJS (Embedded JavaScript)** is a templating engine that allows dynamic content rendering in Express applications. This documentation provides step-by-step instructions on setting up **Express** to use **EJS for** rendering templates. It covers configuring **Express**, setting the view engine, and rendering templates from routes.

## Installing EJS

Before using **EJS** in an **Express** project, install it as a dependency:

```sh
npm install ejs
npm init --y
npm install express ejs
```

## Configuring Express to Use EJS 
Before rendering templates, Express must be configured to recognize EJS as the templating engine.

# Steps

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


