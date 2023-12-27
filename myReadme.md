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

### set up mongoDB 
 * create new project set up everything in mongoDB atlas
#### we use prisma to communicate with our database
 * `npx prisma init`
    * this command create .env file with database url so we put our mongodb url there
    * create prisma folder which consists schema where we connect and create our schema
* create the collection and insert our data manually in our database
* `npx prisma db pull` this tells prisma to see our data and create a model based on our manually inserted data
   * we can see the created schema in schema.prisma file 
   * we can also push our changes from the prisma to our database
* add createdAt and updatedAt models to our collection

N.B := to format our file we use short cut `shift + alt + f`
* `shift + alt + f` and format our prisma file using prima formatter
* our database collection is always plural since it contains multiple datas but for our use this might be confused so we can change the model name in our schema and add @@map to show that changed name alias for the collection name in the db
  `@@map('products')` := this is the previous model name or our db collection name

* `npx prisma db push` to push the update in the prisma to the database
* `npx prisma generate` := this will create prisma client and allow us to use the update schema in our code so, after any update we made we have to run this command.
* Finally we initialize prisma client therefore we can use prisma to manipulate our db in any part of our code. to make it reusable we set up on a separate folder `/lib/db/prisma.tsx`

