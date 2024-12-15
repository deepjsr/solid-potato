# Tailwind CSS Setup Guide

This guide helps you initialize and configure Tailwind CSS in your project.

## Prerequisites

Before starting, ensure you have the following installed:

- **Node.js** (v12 or higher)
- **npm** (Node Package Manager)

## Steps to Set Up Tailwind CSS

### 1. Initialize Tailwind CSS

Run the following command to create the default Tailwind configuration file:

```bash
npx tailwindcss init
```

This generates a `tailwind.config.js` file in your project root directory. Use this file to customize your Tailwind configuration if needed.

---

### 2. Set Up Input and Output CSS Files

Create an `input.css` file inside a `src` folder with the following content:

```css
/* src/input.css */
@tailwind base;
@tailwind components;
@tailwind utilities;
```

This file includes Tailwind's base, components, and utility layers.

---

### 3. Generate the Output CSS File

To process the Tailwind CSS and generate the final output CSS file, run the following command:

```bash
npx tailwindcss -i ./src/input.css -o ./dist/style.css --watch
```

### Command Breakdown:

- **`-i ./src/input.css`**: Specifies the input CSS file.
- **`-o ./dist/style.css`**: Specifies the output CSS file.
- **`--watch`**: Watches for changes in your files and rebuilds the output CSS automatically.

---

## Folder Structure

After following the above steps, your folder structure should look like this:

```
project-root/
├── src/
│   └── input.css
├── dist/
│   └── style.css
├── tailwind.config.js
└── package.json
```

---

## Running Tailwind CSS

1. Open your terminal and run the following command:
   ```bash
   npx tailwindcss -i ./src/input.css -o ./dist/style.css --watch
   ```
2. Tailwind will generate the `style.css` file in the `dist` folder.
3. Keep the terminal running to watch for changes in your `input.css` file.

---

## Using Tailwind CSS

Link the generated `style.css` file in your HTML:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Tailwind CSS Setup</title>
    <link href="./dist/style.css" rel="stylesheet" />
  </head>
  <body>
    <h1 class="text-3xl font-bold text-center">Hello, Tailwind CSS!</h1>
  </body>
</html>
```

Now, you can start using Tailwind CSS classes in your project!

---

## Conclusion

You have successfully set up Tailwind CSS and generated the output CSS file. Use the `--watch` flag to automate the CSS generation while working on your project.

Happy coding! 🚀
