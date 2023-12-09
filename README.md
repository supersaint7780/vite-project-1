# Learning React + Tailwing + Vite

## Step 1 : Project setup
- Install nodejs
- Run the following command to install vite
```bash
npm create vite@latest 
```
- Choose react from template options followed by javascript and other options as per choice
- Initialize the project by running the following commands
```bash
cd <your-project-name>
npm install
npm run dev
```
- To add tailwindcss to the project run the following commands
```bash
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```
- Configure the template paths in the tailwind.config.js
- We also scann css file because the tailwing directives lie there in the index.css file
```javascript
/** @type {import('tailwindcss').Config} */
export default {
  content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx,css}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```
- Add the tailwind directive to your css (./src/index.css file)
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```
- Start the build process
```bash
npm run dev
```
- Start using tailwind css in the project
```javascript
export default function App() {
  return (
    <h1 className="text-3xl font-bold underline">
      Hello world!
    </h1>
  )
}
```

## Step 2 : Folder structure to follow
React and is very versatile in terms of folder structure. Vite's react template comes with a project structure which can be altered to liking.

- Sample project structure to follow
```bash
myproject
- node_modules(folder)
- public(folder)
- src(folder)
--- assets(folder)
----- images(folder)
--- components(folder)
--- App.css
--- App.jsx
--- index.css
--- main.jsx
- other configuration files
```