# ➊ install

```bash
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init tailwind.config.cjs -p
--> Created Tailwind CSS config file: tailwind.config.cjs
--> Created PostCSS config file: postcss.config.js

npm install -D prettier prettier-plugin-tailwindcss
```

## ➋ tailwind.config.cjs 파일 내용 변경

```javascript
/** @type {import('tailwindcss').Config} */
export default {
    content: [], ==> content: ['./src/**/*.{html,js,svelte,ts}'],
    theme: {
        extend: {}
    },
    plugins: []
};
```

## ➌ src/app.css

```css
@tailwind base;
@tailwind components;
@tailwind utilities;

// vscode에서는 플러그인
// PostCSS Language Support를 설치하면 더 이상 경고 문구가 보이지 않는다
```
