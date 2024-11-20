---

# Astro Project Setup

This guide walks you through setting up an Astro project with Tailwind CSS integration.

## Prerequisites

Ensure you have the following installed on your system:

- **Node.js**: v18.17.1, v20.3.0, or higher (v19 is not supported)
- **Text Editor**: We recommend [VS Code](https://code.visualstudio.com/) with the official [Astro extension](https://marketplace.visualstudio.com/items?itemName=astro-build.astro-vscode)
- **Terminal**: Astro is accessed through its command-line interface (CLI)

---

## Project Setup

### 1. Create a New Astro Project

To create a new Astro project, run the following command in your terminal:

```bash
npm create astro@latest
```

Follow the prompts to configure your project as desired.

### 2. Navigate to Your Project Directory

Move into the newly created project directory:

```bash
cd your-project-name
```

### 3. Install Tailwind CSS Integration

Add the Tailwind integration using Astro’s CLI:

```bash
npx astro add tailwind
```

This command automatically installs and configures Tailwind CSS for your Astro project.

### 4. Initialize Tailwind CSS

If you need to make customizations to the Tailwind configuration, you can initialize it with a `tailwind.config.js` file using:

```bash
npx tailwindcss init
```

This creates a `tailwind.config.js` file in your project directory.

### 5. Configure Tailwind CSS Content Paths

Ensure that the content paths are set correctly in the `tailwind.config.js` file:

```javascript
// tailwind.config.js
module.exports = {
  content: ['./src/**/*.{astro,html,js,jsx,md,mdx,svelte,ts,tsx,vue}'],
  theme: {
    extend: {},
  },
  plugins: [],
};
```

### 6. Disable Dev Toolbar (Optional)

If you want to disable the development toolbar, you can do so in `astro.config.mjs`:

```mjs
import { defineConfig } from "astro/config";
import tailwind from "@astrojs/tailwind";

// https://astro.build/config
export default defineConfig({
  integrations: [tailwind()],
  devToolbar: { enabled: false },
});
```

### 7. Start the Development Server

Run the development server using the following command:

```bash
npm run dev
```

### 8. Navigation with Astro Transitions (Optional)

If you are using navigation with transitions, you can import the `navigate` function as shown:

```javascript
import { navigate } from "astro:transitions/client";
```

---

## 9. 🚀 Project Structure

Inside of your Astro project, you'll see the following folders and files:

```text
/
ASTRO-PROJECT/
├── .astro/
├── .vscode/
├── node_modules/
├── public/
├── src/
│   ├── layouts/
│   │   └── Layout.astro
│   ├── pages/
│   │   ├── admin/
│   │   │   └── index.astro
│   │   ├── forgot-password/
│   │   │   └── index.astro
│   │   ├── login/
│   │   │   └── index.astro
│   │   └── register/
│   │       └── index.astro
├── env.d.ts
├── .gitignore
├── astro.config.mjs
├── package-lock.json
├── package.json
├── README.md
├── tailwind.config.js
└── tsconfig.json
```

Astro looks for `.astro` or `.md` files in the `src/pages/` directory. Each page is exposed as a route based on its file name.

There's nothing special about `src/components/`, but that's where we like to put any Astro/React/Vue/Svelte/Preact components.

Any static assets, like images, can be placed in the `public/` directory.

---

## 10. 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |
| `npm run astro ...`       | Run CLI commands like `astro add`, `astro check` |
| `npm run astro -- --help` | Get help using the Astro CLI                     |

---

## Recommended Tools

- **VS Code** with the [Astro extension](https://marketplace.visualstudio.com/items?itemName=astro-build.astro-vscode) for syntax highlighting and other editor enhancements.

---

## Troubleshooting

If you encounter any issues, refer to the [Astro Documentation](https://docs.astro.build/) or open an issue on the [Astro GitHub repository](https://github.com/withastro/astro).

---

## 👀 Want to learn more?

Feel free to check [our documentation](https://docs.astro.build) or jump into our [Discord server](https://astro.build/chat).

Here's a complete step-by-step guideline for setting up an Astro project with Tailwind CSS and all necessary configurations. You can use this content as the basis for your GitHub `README.md` file:

---

With this guideline in your `README.md` file, users will have a clear path to setting up and running their Astro projects with Tailwind CSS integration.
