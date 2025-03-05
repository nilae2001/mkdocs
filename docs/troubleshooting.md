| Symptom | Possible Cause | Solution |
| ------- | -------------- | -------- |
| Partials not rendering in the template | Incorrect path to partial files | Check that the path in `include()` matches your directory structure (e.g., `<%- include('partials/header') %>`) |
| "Error: Cannot find module 'ejs'" when starting server | EJS package not installed | Run `npm install ejs` in your project directory |
| Data not appearing in partials | Data not being passed to the partial | Pass data explicitly to partials: `<%- include('partials/header', { title: 'Home Page' }) %>` |
| "Failed to lookup view" error | Incorrect view directory configuration | Verify `app.set('views', __dirname + '/views')` in your Express configuration |
| Syntax errors in EJS templates | Incorrect EJS tag syntax | Ensure proper syntax: `<%= variable %>` for escaped output, `<%- include() %>` for unescaped output/includes |
| Can't see changes to partials when refreshing browser | Server caching views | Restart the server or implement a development tool like nodemon |
| Template rendering plain text HTML tags | Using `<%= %>` instead of `<%- %>` for HTML content | Use `<%- htmlContent %>` for unescaped HTML rendering |
| Express not recognizing .ejs files | View engine not set to EJS | Add `app.set('view engine', 'ejs')` to your Express configuration |
| "ENOENT: no such file or directory" error | Missing partial file or incorrect file path | Verify the partial file exists and the path is correct relative to the views directory |
| Unable to pass variables to templates | Variables not defined in the route handler | Ensure all needed variables are included in the object passed to `res.render()` |