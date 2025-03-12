+++
title = 'Week 1 - Environment Setup & Basic React Component'
date = 2025-03-12T06:40:21+00:00
draft = false
+++

## Objective

-   Set up your project using Vite and React.
-   Create your very first components (Header, About, Skills, Projects, Footer) for the portfolio
-   Add some basic info about yourself

## Steps

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
    8. Start the development server using: `npm run dev` then ctrl+click on the localhost link that shows up in the terminal to see a demo in your browser.
    - **Problems?** If you encounter errors, verify your Node.js version and installation.
    - **Overwhelmed?** That's totally normal. You're getting thrown in the deep end here. But don't worry, this is 100% within your capabilities, trust me. If you want a deeper look at what each of the files and directories within the project are, then go to the [[#Additional Content Vite Project Structure Overview]] at the bottom of the page for an in-depth breakdown.
    - For now, we'll be focusing primarily on `App.jsx`.
3. **Edit and Create Your First Component**
    1. Delete everything from `App.jsx`, `App.css`, and `index.css`. Vite includes boilerplate code which we won't be needing.
    2. In `App.jsx`, insert the following:

```jsx
export default function App() {
    return <h1>Hello world!</h1>;
}
```

-   This is how you'll end up creating every component from now on: `export default function {ComponentName}`.

    {{< details title="⬅️ Click the triangle for more info `App.jsx`">}}
    This code above is called a _component_. It looks just like a function, but it actually is a powerful way to create reusable pieces of UI in React. Components let you break your interface into independent, manageable parts that can maintain their own state and be easily composed together.

The `App` component is particular is something you'll see in every React app, and serves as the root component for the entire app!

What you're returning in this component looks _a lot_ like HTML, but is actually a different language called "jsx", which essentially just tells JavaScript to insert an `h1` element into `index.html`.
{{< /details >}}

3. Save `App.jsx` and go check out your demo to see your changes. You should see something like this:
   ![Hello World example image](../helloworld.png)

4. Inside the `src` folder, create a new file called `Header.jsx`.

5. Add the following code to `Header.jsx`:

```jsx
export default function Header() {
    return (
        <header>
            <h1>This is the header component</h1>
        </header>
    );
}
```

-   This defines a **new component** called `Header`.
-   It follows the same structure as `App.jsx`, using `export default` so it can be imported elsewhere.

6. Import and use Header inside `App.jsx`:

```jsx
import Header from "./Header"; // This is how we import components

export default function App() {
    return (
        <div>
            <Header /> // This is how we use a component so it appears in our UI
            <h1>Hello world!</h1>
        </div>
    );
}
```

-   You can use Header any number of times in your code. Try copy and pasting `<Header />` a few times and saving `App.jsx` to see what happens.

7. You should see something like this:
   ![Page with basic header component](../headerdone.png)

## Practice Challenge

-   [ ] **Create new components for your About, Skills, Projects, and Footer sections.**

    -   **Hero Section**
        -   Includes a headline, a brief description, and a call-to-action button (like "Contact Me" or "View My Work").
        -   Example input: "Hi, I’m [Your Name], a full-stack developer. I build web apps that solve real problems. Let's work together!"
    -   **About Section:**
        -   Includes an image (e.g., a personal photo or avatar) and three sentences about yourself.
        -   Example input: "Hi, I'm [Your Name], a passionate developer from [Location]. I specialize in React and love tackling challenging problems. In my free time, you’ll find me hiking or working on side projects."
    -   **Skills Section:**
        -   List of technologies or languages you're proficient in (e.g., JavaScript, React, Python).
        -   Example input: A list of skills with accompanying icons or progress bars.
        -   You could create a list or use icons from a library like Font Awesome for each skill.
    -   **Projects Section:**
        -   Showcase a few personal or school projects you've worked on.
        -   Example input: "Project 1: To-Do List App - A simple task manager built with React and Redux. Project 2: Portfolio Website - A personal portfolio built using React and Tailwind CSS."
        -   Each project can have a title, description, and link to the live project or GitHub repository.
    -   **Footer Section:**
        -   Contains contact info, links to your social media profiles, or a copyright notice.
        -   Example input: "Connect with me: [LinkedIn link], [GitHub link], [Email link]." You can also include a copyright message like "© 2025 [Your Name]."

-   [ ] **Import your new components into your `App.jsx`.**
-   [ ] **The challengiest challenge of them all:** if you've completed the previous two challenges and have discovered that you're repeating yourself in your code, then try _extracting that repeated code into their own separate components_. Check out the ![React Docs](https://react.dev/learn/passing-props-to-a-component) on how to pass information to your components.

If you've done all the challenges, it might look like this at the end:
![All challenges done](../challengesdone.png)

Congratulations! At this point, you've created your foundation for your portfolio project. It's not a looker right now, but once we get to styling in the next session so we can really make it pop and look impressive.

To review, we went over how to create a Vite application using npm and node, removed the Vite boilerplate code to insert our own, created our own components and imported them into `App.jsx`, and added information to those components. Check out the [[# Additional Content: Vite Project Structure Overview]] or [[# Additional Content: Other Resources]] to learn more about today.

You've done a great job!

# Additional Content: Vite Project Structure Overview

Below is an explanation of each file and directory in a base Vite + React project:

### 📂 `node_modules/`

This folder contains all the dependencies installed via npm. You generally don’t need to manually edit anything inside this folder. It is automatically generated when you run `npm install`.

### 📂 `public/`

The `public` folder is where static assets (like images, icons, or fonts) are placed. These files won’t be processed by Vite and can be referenced directly in your HTML.

-   📄 `vite.svg`  
    A sample SVG file included with Vite’s default template.

### 📂 `src/`

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

### 🔹 `.gitignore`

Specifies files and folders that Git should ignore, such as `node_modules` and build files.

### 📄 `eslint.config.js`

Configuration file for ESLint, which helps maintain code quality by enforcing coding standards.

### 📄 `index.html`

The main HTML file that Vite serves. It includes a root `<div>` where the React app is injected.

### 📄 `package-lock.json`

Automatically generated file that locks the versions of dependencies for consistency across installations.

### 📄 `package.json`

Defines project metadata, dependencies, scripts, and configurations.

### 📄 `README.md`

A markdown file explaining the project, how to set it up, and how to use it.

### 📄 `vite.config.js`

Configuration file for Vite, allowing customization of the development server and build process.

# Additional Content: Other Resources

### React Docs

The React docs are absolutely _heat_. It's packed with information and examples that will help you get a deeper understanding of how React works and how to use it efficiently. They have examples and challenges in every single part, and if you just spend a few hours going through it you'll be well on your way to knowing _a ton_ about React:  
[React Docs](https://reactjs.org/docs/getting-started.html)

### CSS Box Model

This is for when we start styling our portfolio. You may be surprised to learn that you've got a solid foundation for your portfolio just from this session. However, in order to make the portfolio really pop, you're going to need CSS (we'll be using [Tailwind](https://tailwindcss.com/) next time). Integral to CSS is the box model, so I would recommend brushing up on that here:
[W3Schools Box Model](https://www.w3schools.com/css/css_boxmodel.asp)

### Flexbox Froggy

Also for when we start to style our website, the hardest part is undoubtedly going to be the layout. The CSS `flex` property has made our lives significantly easier, but there's still a bit of a learning curve. Flexbox Froggy will make you a pro at using `flex`/`flexbox` through a fun game:
[Flexbox Froggy](https://flexboxfroggy.com/)
