
# Introduction to EJS

EJS (Embedded JavaScript) is a tool that helps you build HTML pages that adapt based on data or user interactions. It is a way to mix JavaScript directly into your HTML. It is commonly used with Node.js and Express to create dynamic web pages by embedding JavaScript logic inside HTML.

## Intended Audience

This guide is for web developers who have basic knowledge of JavaScript. By the end of this guide, you will know how to create a basic Express app using reusable, dynamic web pages and EJS.

## Prerequisites

To follow these instructions, you will need:

- Basic JavaScript knowledge 
    - Understanding of variables, functions, and loops
- Node.js installed 
    - Download and install [Node.js](https://nodejs.org/en)
- A package manager 
    - Either `npm` (comes with Node.js) or `yarn`
- A code editor 
    - [VS Code](https://code.visualstudio.com/) is recommended
- Basic knowledge of Express.js 
    - Familiarity with setting up a simple server in Express will be helpful

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