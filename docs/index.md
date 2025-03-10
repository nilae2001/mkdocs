
# Introduction to EJS

EJS (Embedded JavaScript) is a powerful templating engine that integrates JavaScript with HTML to create dynamic web content. It allows developers to embed JavaScript code directly within HTML.

EJS is widely adopted in Node.js environments, especially with Express frameworks, thanks to its perfect balance of functionality and straightforward approach.

Key advantages of EJS include:

- Familiar syntax for JavaScript developers
- Fast rendering performance
- Simple integration with Express.js, and other Node.js frameworks
- Support for partials to promote code reusability
- Ability to generate HTML dynamically based on data from other sources

With EJS, developers can create web pages that respond to real-time data while keeping code organized and easy to maintain.

## Intended Audience

This documentation is for developers who are building web applications using Node.js and Express, and want to use EJS (Embedded JavaScript) for rendering dynamic HTML pages. It is designed for individuals who:

- Can write JavaScript code, including using variables, functions, and loops.
- Know HTML and how to structure web pages using elements like headings, paragraphs, lists, and links.
- Have used Node.js, and know how to install and run packages using npm or yarn.
- Understand Express.js and can set up a simple server with route handling.

## Prerequisites

To follow these instructions, you will need:

- Knowledge of JavaScript (ES6) 
    - Understanding of variables, functions, and basic syntax.
- Familiarity with HTML 
    - You should be able to structure web pages using common HTML tags.
- Node.js installed 
    - Download and install [Node.js](https://nodejs.org/en)
- A package manager 
    - Either `npm` (comes with Node.js) or `yarn`.
- A code editor 
    - [VS Code](https://code.visualstudio.com/) is recommended.
- Basic knowledge of Express.js 
    - Familiarity with setting up a simple server in Express will be helpful.

## What You Will Learn

This guide covers:

1. Setting up EJS in a Node.js project
2. Using EJS special syntax to inject dynamic content
3. Integrating EJS with Express for rendering templates
4. Using partials to create reusable components

## Typographical Conventions

| Convention                                     | Example                 |
| ---------------------------------------------- | ----------------------- |
| Bold: Actions are indicated by bolded verbs | **Insert, Click, Enter**|
| Inline Code: Inline code is used to indicate filenames, commands, and short snippets | `views/index.ejs` |

## Admonitions

!!! info "Info"

    Provides additional helpful information.

!!! warning "Warning"

    Highlights potential issues to avoid.

!!! tip "Tip"

    Offers best practices or shortcuts to improve efficiency.
