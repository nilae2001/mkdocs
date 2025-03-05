# EJS Tags

## Overview

EJS uses special tags to dynamically render content in templates, and differentiate between regular HTML and JavaScript logic. This section will cover common EJS tags, and how to use them to output variables, escape HTML, add comments, and more.

---

## EJS Tags and their Usage

EJS provides several types of tags, each serving a distinct purpose.

### `<% %>` - Scriptlet Tag

The Scriptlet Tag is used to execute JavaScript code. These tags are used for control flow and do not output anything to the HTML.

#### Example: A simple `if` Statement

```ejs
<% if(weather.isSunny) { %>
    <p>It's a beautiful day!</p>
<% } %>
```

---

### `<%= %>` - Escaped Output Tag

The Escaped Output Tag is used to output values to the HTML. This tag esapes HTML to prevent cross-site scripting (XSS) attacks.

#### Example: Displaying a User's Name

```ejs
<h1>Welcome, <%= user.name %>!</h1>
```

!!! info "HTML Escaping"

    HTML Escaping converts special characters like `<`, `>`, and `&` into their HTML character entities (`&lt;`, `&gt;`, and `&amp;`). HTML Escaping prevents hackers from injecting malicious code into your webpage.

---

### `<%- %>` - Unescaped Output Tag

The Unescaped Output Tag is similar to the Escaped Output Tag, except that it does not escape HTML. When using these tags, HTML content will be rendered as actual HTML elements.

#### Example: Using Partials to Inject Reusable Components

```ejs
<body>
    <%- include('header') %>
</body>
```

!!! warning "Unescaped HTML"

    Unescaped Output Tags allow raw HTML to be injected into your webpage. This can be dangerous, and should only be used when the content is coming from a trusted source. If a user is allowed to inject unescaped HTML, it could allow XSS attacks

---

### `<%# %>` - Comment Tag

The Comment Tag is used to write comments in EJS files. Comments made using the comment tag will not be visible in the source code. These tags can be used to hide notes or explanations.

#### Example: Adding a Comment

```ejs
<%# This is an EJS comment %>
```

!!! tip "HTML Comments"

    To make a comment visible in the source code, use:

    ```ejs
    <!-- This comment is visible in the source code -->
    ```

---

### `<%%` and `%%>` - Literal Tags

The Literal Tag is used to output a raw EJS tag. These tags escape the EJS, and display `<%` and `%>` as plain text in the browser.

#### Example: Displaying an Example of EJS Escaped Output Tag

```ejs
<%%= "This will print <%= pet.name %>" %%>
```

#### HTML Output
```html
<%= pet.name %>
```

---

## Conclusion

EJS provides flexible syntax for embedding JavaScript logic within HTML. By following this guide and being aware of security concerns, you can use these tags to effectively create dynamic web pages

### Summary of EJS Tags

| EJS Tag         | Usage                                  |
| --------------- | -------------------------------------- |
| `<% %>`         | Logic (conditional statements, loops)  |
| `<%= %>`        | Safe (escaped) content injection       |
| `<%- %>`        | Raw (unescaped) content injection      |
| `<%# %>`        | Comments                               |
| `<%%` and `%%>` | Displaying `<%` and `%>` as plain text |