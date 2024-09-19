# 🎉 Birthday Celebration 3D Web Scene - React + TypeScript + Vite 🎉

This project showcases a fun, interactive 3D web scene created with **Spline** and integrated into a **React** project powered by **Vite**. The scene celebrates birthdays with some fun user interactions like playing a Happy Birthday song and blowing out a candle. Plus, there’s a hidden **easter egg** for users to discover! 🕵️‍♂️🔍

[Live Demo](https://happy-birthday-spline.netlify.app)

<img width="1468" alt="image" src="https://github.com/user-attachments/assets/b8484c39-8ed5-42fd-b228-5db232d4449d">

---

## 🚀 Tech Stack

- **React** with **TypeScript**
- **Vite** for fast development and build times
- **Spline** for 3D scene creation
- **Netlify** for deployment
- **ESLint** for code linting
- **GitHub** for version control and project hosting

---

## 🛠 Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/safciezgi/happy-birthday-spline.git
cd your-repo-name
```
### 2. Install dependencies

```bash
npm install
```
### 3. Run the development server

```bash
npm run dev
```
### 4. Build for production

```bash
npm run build
```
### 5. Preview the production build

```bash
npm run preview
```

---

## 🔍 Features

- **Interactive 3D Scene**: Explore the birthday celebration with interactions like playing the Happy Birthday song and blowing out the candle.
- **Easter Egg**: Can you find the hidden surprise? 🕵️‍♂️
- **Fast Development Setup**: Powered by **Vite**, with HMR (Hot Module Replacement) for a smooth development experience.

---

## 🧩 React + TypeScript + Vite Configuration

This project is based on the **React + TypeScript + Vite** template, which provides a minimal setup with HMR and some ESLint rules.

### Key Plugins:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh.
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh.

### Expanding the ESLint Configuration

If you’re developing a production application, we recommend enabling type-aware lint rules for stricter type checking:

1. Update the top-level `parserOptions` property like this:

    ```js
    export default tseslint.config({
      languageOptions: {
        // other options...
        parserOptions: {
          project: ['./tsconfig.node.json', './tsconfig.app.json'],
          tsconfigRootDir: import.meta.dirname,
        },
      },
    })
    ```

2. Replace `tseslint.configs.recommended` with `tseslint.configs.recommendedTypeChecked` or `tseslint.configs.strictTypeChecked`.
3. Optionally, add `...tseslint.configs.stylisticTypeChecked`.
4. Install [eslint-plugin-react](https://github.com/jsx-eslint/eslint-plugin-react) and update your ESLint config like this:

    ```js
    // eslint.config.js
    import react from 'eslint-plugin-react'

    export default tseslint.config({
      // Set the React version
      settings: { react: { version: '18.3' } },
      plugins: {
        // Add the react plugin
        react,
      },
      rules: {
        // Enable recommended rules
        ...react.configs.recommended.rules,
        ...react.configs['jsx-runtime'].rules,
      },
    })
    ```
