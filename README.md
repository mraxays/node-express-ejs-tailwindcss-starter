# Node.js Express EJS Tailwind CSS Starter

A starter template for building modern web applications using **Node.js**, **Express.js**, **EJS**, and **Tailwind CSS**.

## Features

* Express.js server setup
* EJS templating for dynamic web pages
* Tailwind CSS integration for styling
* Organized project structure with routes, views, and public assets
* Ready-to-use middleware for request parsing
* Development workflow with Nodemon and Tailwind CSS watch mode
* Production-ready CSS build process

## Project Structure

```text
NODE-EXPRESS-EJS-TAILWINDCSS-STARTER
│
├── bin/
│   └── www                    # Server start script
│
├── public/
│   ├── images/                # Image files
│   ├── javascripts/           # Client-side JavaScript files
│   └── stylesheets/
│       └── tailwind.css       # Tailwind CSS source file
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
├── app.js                     # Main application file
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

## Build for Production

To compile and minify the Tailwind CSS for production:

```sh
npm run buildcss
```

## Usage

### Customize the Homepage

Modify:

```text
views/index.ejs
```

to customize the application's homepage.

### Add New Routes

Create or modify route files inside:

```text
routes/
```

Then register the routes in:

```text
app.js
```

### Customize Tailwind CSS

Edit:

```text
public/stylesheets/tailwind.css
```

to add or customize your styles.

### Run Tailwind CSS in Development

Use:

```sh
npm run devcss
```

to compile Tailwind CSS and watch for changes.

### Run the Development Server

Use:

```sh
npm run dev
```

to start the development environment with automatic server restarts.

## Dependencies

The project uses the following dependencies:

* **Express.js** — Web application framework
* **EJS** — Embedded JavaScript templating engine
* **Tailwind CSS** — Utility-first CSS framework
* **Morgan** — HTTP request logger
* **Cookie Parser** — Cookie parsing middleware
* **Debug** — Debugging utility
* **HTTP Errors** — HTTP error creation and handling
* **@tailwindcss/cli** — Tailwind CSS command-line interface

## Development Dependencies

The project includes the following development dependencies:

* **Nodemon** (`^3.1.9`) — Automatically restarts the server when files change
* **Prettier** (`^3.5.3`) — Code formatting
* **Prettier Plugin Tailwind CSS** (`^0.6.11`) — Tailwind CSS class sorting and formatting

## Available Scripts

| Command              | Description                                                                |
| -------------------- | -------------------------------------------------------------------------- |
| `npm start`          | Start the application normally                                             |
| `npm run dev`        | Start the development environment with Nodemon and Tailwind CSS watch mode |
| `npm run devcss`     | Compile Tailwind CSS and watch for changes                                 |
| `npm run dev:server` | Start the development server                                               |
| `npm run buildcss`   | Build and minify Tailwind CSS                                              |

## Configuration

Before using the starter template, update the `name` field in `package.json`:

```json
{
  "name": "your-project-name"
}
```

Replace `your-project-name` with the name of your application.

## License

This project is licensed under the [MIT License](LICENSE.md).

## Contributions and Support

Contributions are welcome.

If you find a bug, have a suggestion, or would like to improve the starter template, feel free to open an issue or submit a pull request.
