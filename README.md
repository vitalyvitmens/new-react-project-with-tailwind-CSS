1. https://tailwindcss.com/docs/installation
2. cd my-app
3. npm i -D tailwindcss
4. npx tailwindcss init
5. В файл tailwind.config.js добавить:

/** @type {import('tailwindcss').Config} */
export const content = ['./src/**/*.{html,js}']
export const theme = {
	extend: {},
}
export const plugins = []

6. В файл index.css добавьте директивы:

@tailwind base;
@tailwind components;
@tailwind utilities;

@layer components {
	.circle-red {
		@apply m-auto; /* круг по центру установить вместо margin: auto; */
		width: 200px;
		height: 200px;
		border-radius: 50%;
		border: 5px solid black;
		background-color: red;
		/* margin: auto; */
		margin-top: 5rem;
		font-size: 7rem;
		font-weight: 500;
		padding-top: 10px;
	}
}

7. установи расширение для VS Code: Tailwind CSS IntelliSense
8. npm run start
