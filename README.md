### create vite vanilla js

[https://vitejs.dev/guide/#scaffolding-your-first-vite-project](https://vitejs.dev/guide/#scaffolding-your-first-vite-project)

```
yarn create vite filename --template vanilla
cd filename
yarn
yarn dev
```

### tailwindcss

[https://tailwindcss.com/docs/guides/vite](https://tailwindcss.com/docs/guides/vite)

```
yarn add -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

### update tailwind.config.js

```js
/** @type {import('tailwindcss').Config} */
export default {
  content: ['./index.html', './src/**/*.{js,ts,jsx,tsx}'],
  theme: {
    extend: {}
  },
  plugins: []
}
```

### update style.css

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

### vite.config.js

```
touch vite.config.js
```

### update vite.config.js

```js
import { resolve } from 'path'
import { defineConfig } from 'vite'

export default defineConfig({
  build: {
    rollupOptions: {
      input: {
        main: resolve(__dirname, 'index.html'),
        about: resolve(__dirname, 'about/index.html')
      }
    }
  }
})
```

### create about folder

```
mkdir about
touch about/index.html
```
