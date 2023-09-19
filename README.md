# LESS Compilation with Source Maps

This guide will walk you through the process of compiling LESS files with source maps, which can be helpful for debugging in a development environment.

## Prerequisites

**Node.js:** Ensure you have Node.js installed. If not, you can download and install it from the Node.js official website.

**LESS Compiler:** Once Node.js is installed, you'll need the LESS compiler. Install it globally using npm (Node Package Manager):

 ```
npm install -g less
 ```
## Compiling LESS with Source Maps

Open your terminal or command prompt and navigate to the directory containing your LESS file.

 ```
cd path/to/your/directory
 ```

Use the lessc command followed by the name of your LESS file and the desired output name for the CSS file. Add the --source-map option to generate a source map.

 ```
lessc styles.less styles.css --source-map
 ```

After running the command, you should see two new files in your directory:

- styles.css: The compiled CSS.
- styles.css.map: The source map for the CSS.

Link to the generated styles.css file in your HTML document:

 ```
<link rel="stylesheet" href="styles.css" />
 ```

Open your HTML file in a browser. When you inspect an element styled by styles.css, the browser's developer tools will show the original LESS code (ensure source maps are enabled in the developer tools settings).

Note:
Ensure the source map (styles.css.map) is in the same directory as the compiled CSS (styles.css) for correct mapping.
