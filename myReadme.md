# Gebeya E-commerce Application with NextJs

### project setup
 * `npx create-next-app@latest`
 * we use tailwind css and typescript for development
 * install tailwind intellisense and adjust some vs code settings
 * file: association => add `*.css` as item `tailwindcss` as value
 * quick suggesition `string : on`
 * dependecies installed 
  ```
  * daisyui * prisma  * next-auth * @prisma/client * prettier * eslint-config-prettier * prettier-plugin-tailwindcss
  ```

  * prettier tailwind css plugin used for class name sorting to the recommended order
#### to set up prettier tailwind css plugin
 * create a config file `prettier.config.js` and add
 * 
   ```
   module.exports = {
         plugins: [require("prettier-plugin-tailwindcss")],
      };
      ```

* to make sure eslint and prettier don't conflict with eachother add "prettier" in eslint.json `"extends": ["next/core-web-vitals", "prettier"]`
* add vs code extensions
   * eslint := to see warnings in our code
   * prisma := prisma orm extension
* install a package called zod `npm i zod`
  
