# Node.js Express EJS Tailwind CSS Starter

![License](https://img.shields.io/badge/License-MIT-ff932e)
![Release](https://img.shields.io/github/v/release/mraxays/node-express-ejs-tailwindcss-starter?color=ff7a5e)

A starter template for building modern web applications using **Node.js**, **Express.js**, **EJS**, and **Tailwind CSS**.

## Features

* Express.js server setup
* ES Modules (`import` / `export`) with `"type": "module"`
* EJS templating for dynamic web pages
* Tailwind CSS v4 integration for styling
* Organized project structure with routes, views, and public assets
* Ready-to-use middleware for request parsing, cookies, static files, and request logging
* Built-in 404 and error handling with a custom error page
* Configurable port through the `PORT` environment variable
* Development workflow with Nodemon and Tailwind CSS watch mode
* Production-ready CSS build process

## Module System

This starter uses **ES Modules** (since v2.0.0). If you need the **CommonJS** version, use the [v1.0.0 release](https://github.com/mraxays/node-express-ejs-tailwindcss-starter/releases/tag/v1.0.0).

## Requirements

* Node.js 20 or later

## Project Structure

```text
NODE-EXPRESS-EJS-TAILWINDCSS-STARTER
│
├── bin/
│   └── www                    # Server start script (HTTP server, port, error handling)
│
├── public/
│   ├── images/                # Image files
│   ├── javascripts/           # Client-side JavaScript files
│   └── stylesheets/
│       ├── tailwind.css       # Tailwind CSS source file (edit this)
│       └── styles.css         # Compiled CSS output (generated)
│
├── routes/
│   ├── index.js               # Main application routes
│   └── users.js               # Example user routes
│
├── views/
│   ├── index.ejs              # Main page
│   └── error.ejs              # Error page
│
├── .gitignore
├── .prettierrc
├── app.js                     # Express app setup (middleware, routes, error handling)
├── LICENSE.md
├── package.json
├── package-lock.json
└── README.md
```

> `node_modules/` is generated automatically when dependencies are installed and should not be committed to the repository.

## Installation

### 1. Clone the Repository

```sh
git clone git@github.com:mraxays/node-express-ejs-tailwindcss-starter.git
cd node-express-ejs-tailwindcss-starter
```

### 2. Install Dependencies

```sh
npm install
```

### 3. Start the Server

```sh
npm start
```

The server will run at:

```text
http://localhost:3000/
```

## How It Works

### `bin/www`

Starts the HTTP server. It imports the Express app from `app.js`, reads the port from the `PORT` environment variable (default `3000`), and handles common startup errors such as a port already in use (`EADDRINUSE`).

### `app.js`

Creates and configures the Express app:

* Sets EJS as the view engine and `views/` as the views folder
* Adds middleware: Morgan (request logging), `express.json()`, `express.urlencoded()`, Cookie Parser, and static file serving from `public/`
* Registers the routes (`/` and `/users`)
* Forwards unknown URLs to a 404 error, and renders `views/error.ejs` for all errors
* Exports the app with `export default app`

### `routes/` and `views/`

`routes/index.js` renders `views/index.ejs` and passes a `title` value:

```js
router.get("/", function (req, res, next) {
  res.render("index", { title: "Express" });
});
```

`views/index.ejs` displays the title with `<%= title %>`, uses Tailwind CSS classes for styling, and loads the compiled stylesheet:

```html
<link rel="stylesheet" href="/stylesheets/styles.css" />
```

## Development

### Development with Auto-Reloading

To run the development environment with Nodemon and Tailwind CSS watch mode:

```sh
npm run dev
```

### Tailwind CSS Watch Mode

To compile Tailwind CSS and watch for changes:

```sh
npm run devcss
```

### Development Server

To run only the development server:

```sh
npm run dev:server
```

## Configuration

### Project Name

Before using the starter template, update the `name` field in `package.json`:

```json
{
  "name": "your-project-name"
}
```

Replace the default `projectname` with the name of your application.

### Change the Port

The server uses the `PORT` environment variable and falls back to `3000`.

macOS / Linux:

```sh
PORT=4000 npm start
```

Windows (PowerShell):

```powershell
$env:PORT=4000; npm start
```

### Environment Variables with dotenv (Optional)

`bin/www` includes commented-out `dotenv` lines. To use a `.env` file:

1. Install the package:

   ```sh
   npm install dotenv
   ```

2. Uncomment these lines at the top of `bin/www`:

   ```js
   import dotenv from 'dotenv';
   dotenv.config();
   ```

3. Create a `.env` file in the project root with the following content:

   ```text
   PORT=4000
   ```

## Usage

### Customize the Homepage

Modify:

```text
views/index.ejs
```

to customize the application's homepage. To change the page title, edit the `title` value in `routes/index.js`.

### Add New Routes

Create a route file inside `routes/`:

```js
// routes/products.js
import express from "express";

const router = express.Router();

router.get("/", (req, res) => {
  res.render("index", { title: "Products" });
});

export default router;
```

Then register it in `app.js`:

```js
import productsRouter from "./routes/products.js";

app.use("/products", productsRouter);
```

> Relative imports must include the `.js` extension in ES Modules.

### Customize Tailwind CSS

Edit:

```text
public/stylesheets/tailwind.css
```

to add or customize your styles.

> `public/stylesheets/styles.css` is the compiled output generated by `npm run devcss` and `npm run buildcss`. Don't edit it by hand.

### Using `__dirname` in ES Modules

`__dirname` and `__filename` are not available in ES Modules. `app.js` defines them like this:

```js
import { fileURLToPath } from "url";
import { dirname } from "path";

const __filename = fileURLToPath(import.meta.url);
const __dirname = dirname(__filename);
```

On Node.js 20.11+ you can also use `import.meta.dirname` directly.

## Build for Production

To compile and minify the Tailwind CSS for production:

```sh
npm run buildcss
```

## Updating Dependencies

### Update Package Versions

You can use `npm-check-updates` to check for and update dependency versions:

```sh
npx npm-check-updates -u
```

After updating `package.json`, install the updated dependencies:

```sh
npm install
```

## Dependencies

The project uses the following dependencies:

* **Express.js** (v5) — Web application framework
* **EJS** (v6) — Embedded JavaScript templating engine
* **Tailwind CSS** (v4) — Utility-first CSS framework
* **@tailwindcss/cli** — Tailwind CSS command-line interface
* **Morgan** — HTTP request logger
* **Cookie Parser** — Cookie parsing middleware
* **Debug** — Debugging utility
* **HTTP Errors** — HTTP error creation and handling

## Development Dependencies

* **Nodemon** — Automatically restarts the server when files change
* **Concurrently** — Runs the server and Tailwind CSS watch mode together
* **Prettier** — Code formatting
* **Prettier Plugin Tailwind CSS** — Tailwind CSS class sorting and formatting

## Available Scripts

| Command              | Description                                                                |
| -------------------- | -------------------------------------------------------------------------- |
| `npm start`          | Start the application normally                                             |
| `npm run dev`        | Start the development environment with Nodemon and Tailwind CSS watch mode |
| `npm run devcss`     | Compile Tailwind CSS and watch for changes                                 |
| `npm run dev:server` | Start the development server                                               |
| `npm run buildcss`   | Build and minify Tailwind CSS                                              |

## License

This project is licensed under the [MIT License](LICENSE.md).

## Contributions and Support

Contributions are welcome.

If you find a bug, have a suggestion, or would like to improve the starter template, feel free to open an issue or submit a pull request.