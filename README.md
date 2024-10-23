# nl4
Another copilot game test

## Setting up ViteJS with Yarn

To set up ViteJS for a vanilla Typescript app using Yarn, follow these steps:

1. Install Yarn if you haven't already:
   ```sh
   npm install --global yarn
   ```

2. Create a new project directory and navigate into it:
   ```sh
   mkdir my-vite-app
   cd my-vite-app
   ```

3. Initialize a new Yarn project:
   ```sh
   yarn init -y
   ```

4. Add ViteJS and Typescript as dependencies:
   ```sh
   yarn add vite typescript
   ```

5. Create a `tsconfig.json` file for Typescript configuration:
   ```json
   {
     "compilerOptions": {
       "target": "esnext",
       "module": "esnext",
       "moduleResolution": "node",
       "strict": true,
       "jsx": "preserve",
       "esModuleInterop": true,
       "skipLibCheck": true,
       "forceConsistentCasingInFileNames": true
     },
     "include": ["src"]
   }
   ```

6. Create a `vite.config.ts` file for ViteJS configuration:
   ```ts
   import { defineConfig } from 'vite'

   export default defineConfig({
     root: 'src',
     build: {
       outDir: '../dist'
     }
   })
   ```

7. Create a `src` directory and add an `index.html` file:
   ```html
   <!DOCTYPE html>
   <html lang="en">
   <head>
     <meta charset="UTF-8">
     <meta name="viewport" content="width=device-width, initial-scale=1.0">
     <title>Vite App</title>
   </head>
   <body>
     <script type="module" src="/main.ts"></script>
   </body>
   </html>
   ```

8. Add a `main.ts` file in the `src` directory:
   ```ts
   console.log('Hello Vite with Typescript!')
   ```

9. Add scripts to `package.json` for running the development server and building the project:
   ```json
   {
     "scripts": {
       "dev": "vite",
       "build": "vite build"
     }
   }
   ```

10. Run the development server:
    ```sh
    yarn dev
    ```

11. Build the project:
    ```sh
    yarn build
    ```
