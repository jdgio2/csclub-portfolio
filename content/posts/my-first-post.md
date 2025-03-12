+++
title = 'Week 1 - Environment Setup & Basic React Component'
date = 2025-03-12T06:40:21+00:00
draft = false
+++

### Objective

-   Set up your project using Vite and React.
-   Create your very first components (Header, About, Skills, Projects, Footer) for the portfolio
-   Add basic information for

### Steps

1. **Install Prerequisites**
    - Ensure Node.js is installed on your computer.
        - Use `node --version` in your terminal to check if it's installed properly.
2. **Create a New Vite Project**
    1. Open your terminal and run: `npm create vite@latest`
    2. Enter the name of your project and then hit enter. I'll be naming mine `awesome-portfolio`
    3. When asked to pick a framework, select `React` using the arrow keys and hit enter.
    4. When asked to select a variant, select `JavaScript` using the arrow keys and hit enter.
    5. If you haven't already, open your project in VSCode typing `code ./awesome-portfolio` in your terminal (if it's set up in your PATH, don't worry if it doesn't work) or by launching VSCode, going to "File" > "Open Folder..." > and selecting the location where you created your portfolio.
    6. Open your terminal in VSCode by hitting "Terminal" in the top left menu and clicking "New Terminal".
    7. Install all dependencies by typing `npm install`. You might be asked if it's okay to install Vite (or maybe some npm things). If so, keep hitting enter to accept them and start installing.
    8. Start the development server using: `npm run dev`
    - **Problems?** If you encounter errors, verify your Node.js version and installation.
3. **Project Structure Explained**
    - Key folders:
      `src/`
      `public/`
4. **Create Your First Component**

    - Create a file:
      `src/components/Header.jsx`
    - Add the following code:

```jsx
import React from "react";

const Header = () => {
    return (
        <header>
            <h1>My Portfolio</h1>
        </header>
    );
};

export default Header;
```

-   Import and render
-

5. **Practice Challenge**
    - Create a new components for your About, Skills, Projects, and Footer sections.
    - Import into your `App.jsx`

# Vite Project Structure Overview

In this tutorial, we will go over the structure of a typical Vite + React project. Below is an explanation of each file and directory:

## 📂 `node_modules/`

This folder contains all the dependencies installed via npm. You generally don’t need to manually edit anything inside this folder. It is automatically generated when you run `npm install`.

## 📂 `public/`

The `public` folder is where static assets (like images, icons, or fonts) are placed. These files won’t be processed by Vite and can be referenced directly in your HTML.

-   📄 `vite.svg`  
    A sample SVG file included with Vite’s default template.

## 📂 `src/`

This is where the main application code lives.

-   📂 `assets/`

    -   📄 `react.svg`  
        Another sample SVG file, typically used as the React logo.

-   📄 `App.css`  
    Styles for the `App.jsx` component.

-   📄 `App.jsx`  
    The main React component, serving as the entry point for the UI.

-   📄 `index.css`  
    Global CSS styles that apply to the whole app.

-   📄 `main.jsx`  
    The file where the React app is initialized and rendered into the DOM.

## 🔹 `.gitignore`

Specifies files and folders that Git should ignore, such as `node_modules` and build files.

## 📄 `eslint.config.js`

Configuration file for ESLint, which helps maintain code quality by enforcing coding standards.

## 📄 `index.html`

The main HTML file that Vite serves. It includes a root `<div>` where the React app is injected.

## 📄 `package-lock.json`

Automatically generated file that locks the versions of dependencies for consistency across installations.

## 📄 `package.json`

Defines project metadata, dependencies, scripts, and configurations.

## 📄 `README.md`

A markdown file explaining the project, how to set it up, and how to use it.

## 📄 `vite.config.js`

Configuration file for Vite, allowing customization of the development server and build process.
