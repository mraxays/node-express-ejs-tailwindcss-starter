# Node-Express-EJS-TailwindCSS Starter

A starter template for building web applications with **Node.js**, **Express**, **EJS**, and **Tailwind CSS**.

## Features
- 🚀 **Express.js** server setup
- 🎨 **EJS templating** for dynamic web pages
- 💨 **Tailwind CSS** integration for styling
- 📂 Organized project structure (routes, views, public assets)
- 🛠 Ready-to-use middleware for request parsing

## Project Structure
```
NODE-EXPRESS-EJS-TAILWINDCSS-STARTER
│── bin/                     # Server start script (if applicable)
│── node_modules/            # Dependencies (ignored in repo)
│── public/                  # Static assets (CSS, JS, Images)
│   ├── images/              # Image files
│   ├── javascripts/         # JavaScript files
│   ├── stylesheets/         # CSS files (includes Tailwind)
│── routes/                  # Express route handlers
│   ├── index.js             # Main route
│   ├── users.js             # Example user route
│── views/                   # EJS templates
│   ├── index.ejs            # Main page
│   ├── error.ejs            # Error page
│── .gitignore               # Ignored files
│── .prettierrc              # Code formatting rules
│── app.js                   # Main application file
│── LICENSE.md               # License file
│── package.json             # Project dependencies
│── package-lock.json        # Dependency lock file
│── README.md                # Documentation
```

## Installation
1. Clone the repository:
   ```sh
   git clone https://github.com/mraxays/node-express-ejs-tailwindcss-starter.git
   cd node-express-ejs-tailwindcss-starter
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Start the development server:
   ```sh
   npm start
   ```
   The server runs at `http://localhost:3000/` by default.

## Usage
- Modify **views/index.ejs** to customize the homepage.
- Add new routes in **routes/** and link them in **app.js**.
- Edit **public/stylesheets/tailwind.css** for custom styling.

## License
This project is licensed under the [MIT License](LICENSE.md).

---

### Contributions & Support
Feel free to submit issues or pull requests to improve this starter template!

