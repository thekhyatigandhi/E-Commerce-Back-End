# E-COMMERCE BACK END </br>

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Node.js Badge](https://img.shields.io/badge/Node.js-393?logo=nodedotjs&logoColor=fff&style=flat)](https://nodejs.org/en)
[![MySQL Badge](https://img.shields.io/badge/MySQL-4479A1?logo=mysql&logoColor=fff&style=flat)](https://www.npmjs.com/package/mysql2)
[![Sequelize Badge](https://img.shields.io/badge/Sequelize-52B0E7?logo=sequelize&logoColor=fff&style=flat)](https://sequelize.org/docs/v6/)
[![.ENV Badge](https://img.shields.io/badge/.ENV-ECD53F?logo=dotenv&logoColor=000&style=flat)](https://www.npmjs.com/package/dotenv)
[![Nodemon Badge](https://img.shields.io/badge/Nodemon-76D04B?logo=nodemon&logoColor=fff&style=flat)](https://nodemon.io/)
[![Insomnia Badge](https://img.shields.io/badge/Insomnia-4000BF?logo=insomnia&logoColor=fff&style=flat)](https://insomnia.rest/)

## Description

This is an E-commerce back end for a website where the code syncs Sequalize models to MySQL database on the server start and it includes column definition for all four models and model associations and provides the following GET, POST, PUT and DELETE routes. </br>

**Category**

GET all categories, GET a single category by ID, POST(create) a new category, PUT(update) and existing category by ID, and DELETE an existing category by ID.

**Tag**

GET all tags, GET a single tag by ID, POST(create) a new tag, PUT(update) an existing tag by ID, and DELETE an existing tag by ID.

**Product (including ProductTag)**

GET all products, GET products by ID, and DELETE products by ID. POST(create) and PUT(update) product routes were provided in starter code.

- [Application](#Application)
- [Technologies Used](#TechnologiesUsed)
- [Installation](#Installation)
- [Usage](#usage)
- [Credits](#credits)
- [License](#license)

## Application

The following [video] (https://youtu.be/Yw5SnOgDlVI) shows the application's set-up in VScode and demonstarted all API routes using Insomnia.

## Technologies Used

MySQL </br>
NODE JS </br>
Insomnia

## Installation

## Installation

- Check if you have Node.js installed by typing `node -v` in your command line. If node is not installed, visit the [Node.js](https://nodejs.org/en) website to install.
- Next, clone this project repository to your computer.
- Use the command `npm i` to install dependencies.
- Create a file in the root directory titled `.env` and include database name and personal MySQL login information:

```
DB_NAME='YOUR DATABASE NAME'
DB_USER='YOUR USERNAME'
DB_PW='YOUR PASSWORD'
```

- Open MySQL with command `mysql -u root -p` and enter your personal MySQL password.
- Create databse with command `source schema.sql`. Log out of MySQL with command `\q`.
- Seed database with command `npm run seed`.

## Usage

- Start server with command `npm start`.
- Alternatively, start server with Nodemon (and restart server automatically when making changes to code) with command `npm run watch`.
- Access API routes with Insomnia using the following endpoints:

|                                  | CATEGORY                                 | TAG                                | PRODUCT                                |
| -------------------------------- | ---------------------------------------- | ---------------------------------- | -------------------------------------- |
| GET (ALL), POST(CREATE)          | http://localhost:3001/api/categories/    | http://localhost:3001/api/tags/    | http://localhost:3001/api/products/    |
| GET (BY ID), PUT(UPDATE), DELETE | http://localhost:3001/api/categories/:id | http://localhost:3001/api/tags/:id | http://localhost:3001/api/products/:id |

- Make POST and PUT requests with the following JSON body formats:

  **CATEGORY**

  ```
  {
  "categoryName": "STRING INPUT"
  }
  ```

  **TAG**

  ```
  {
  "tagName": "STRING INPUT"
  }
  ```

  **PRODUCT**

  ```
  {
  "product_name": "STRING INPUT",
  "price": DECIMAL INPUT,
  "stock": INTEGER INPUT,
  "tagIds": INTEGER INPUT
  }
  ```

## Credits

https://nodejs.org/en </br>
https://www.youtube.com/watch?v=7S_tz1z_5bA </br>
https://www.youtube.com/watch?v=pxo7L5nd1gA

## License

MIT License.
For more information on the license, please refer to the LICENSE file in the repo
