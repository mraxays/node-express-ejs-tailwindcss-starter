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
│── package.json             # Project dependencies (Update name "projectname" to your actual project name)
│── package-lock.json        # Dependency lock file
│── README.md                # Documentation
```

## Installation
1. Clone the repository:
   ```sh
   git clone git@github.com:mraxays/node-express-ejs-tailwindcss-starter.git
   cd node-express-ejs-tailwindcss-starter
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Start the server:
   ```sh
   npm start
   ```
   The server runs at `http://localhost:3000/` by default.

3.1 For development with auto-reloading (Tailwind CSS watching & Nodemon):
   ```sh
   npm run dev
   ```
3.2 For development with Tailwind CSS watching:
   ```sh
   npm run devcss
   ```
3.3 For Running development server
   ```sh
   npm run dev:server
   ```
4. Update Package:
   ```sh
   npx npm-check-updates -u
   ```
If you want to update all dependencies to the latest versions.
4.1 Update dependencies:
   ```sh
   npm install
   ```
5. For building the project with minified CSS:
   ```sh
   npm run buildcss
   ```
## Usage
- Modify **views/index.ejs** to customize the homepage.
- Add new routes in **routes/** and link them in **app.js**.
- Edit **public/stylesheets/tailwind.css** for custom styling.
- Update **package.json** and change the name "projectname" to your actual project name.
- Use **npm run devcss** to compile Tailwind CSS.
- Use **npm run dev** to start the server with Nodemon for auto-reloading.

## Dependencies
This project includes the following dependencies:
- **Express** 
- **EJS** 
- **Tailwind CSS** 
- **Morgan** (for logging)
- **Cookie Parser** (for handling cookies)
- **Debug** (for debugging)
- **HTTP Errors** (for error handling)
- **@tailwindcss/cli** (for Tailwind CLI)

## Dev Dependencies
- **Nodemon** (`^3.1.9` for auto-restarting the server)
- **Prettier** (`^3.5.3` for code formatting)
- **Prettier Plugin TailwindCSS** (`^0.6.11` for Tailwind-specific formatting)

## Scripts
The following scripts are available:
- **npm start** - Start the server normally.
- **npm run dev** - Start the server with **Nodemon** for auto-restarting.
- **npm run devcss** - Compile **Tailwind CSS** and watch for changes.

## License
This project is licensed under the [MIT License](LICENSE.md).

---

### Contributions & Support
Feel free to submit issues or pull requests to improve this starter template!

