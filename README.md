# ECommerce Backend Project 2023

## Your Task

Internet retail, also known as **e-commerce**, plays a significant role within the electronics industry, as it empowers businesses and consumers alike to conveniently engage in online buying and selling of electronic products. In the latest available data from 2021, the industry in the United States alone was estimated to have generated the substantial amount of US$2.54 trillion, according to the United Nations Conference on Trade and Development. E-commerce platforms like Shopify and WooCommerce provide a suite of services to businesses of all sizes. Due to the prevalence of these platforms, developers should understand the fundamental architecture of e-commerce sites.

Your task is to build the back end for an e-commerce site by modifying starter code. You’ll configure a working Express.js API to use Sequelize to interact with a MySQL database.

Because this application won’t be deployed, you’ll also need to provide a link to a walkthrough video that demonstrates its functionality and all of the acceptance criteria being met. You’ll need to submit a link to the video and add it to the readme of your project.

## User Story

```md
AS A manager at an internet retail company
I WANT a back end for my e-commerce website that uses the latest technologies
SO THAT my company can compete with other e-commerce companies
```

## Acceptance Criteria

```md
GIVEN a functional Express.js API
WHEN I add my database name, MySQL username, and MySQL password to an environment variable file
THEN I am able to connect to a database using Sequelize
WHEN I enter schema and seed commands
THEN a development database is created and is seeded with test data
WHEN I enter the command to invoke the application
THEN my server is started and the Sequelize models are synced to the MySQL database
WHEN I open API GET routes in Insomnia for categories, products, or tags
THEN the data for each of these routes is displayed in a formatted JSON
WHEN I test API POST, PUT, and DELETE routes in Insomnia
THEN I am able to successfully create, update, and delete data in my database
```

## Mock-Up

The following animation shows the application's GET routes to return all categories, all products, and all tags being tested in Insomnia:

![In Insomnia, the user tests “GET tags,” “GET Categories,” and “GET All Products.”.](./Assets/13-orm-homework-demo-01.gif)

The following animation shows the application's GET routes to return a single category, a single product, and a single tag being tested in Insomnia:

![In Insomnia, the user tests “GET tag by id,” “GET Category by ID,” and “GET One Product.”](./Assets/13-orm-homework-demo-02.gif)

The following animation shows the application's POST, PUT, and DELETE routes for categories being tested in Insomnia:

![In Insomnia, the user tests “DELETE Category by ID,” “CREATE Category,” and “UPDATE Category.”](./Assets/13-orm-homework-demo-03.gif)

## Installation

The schema.sql contributes the following:

-The schema contributes the initial creation of the database (ecommerce_db).

The server.js contributes the following:

-Defines the use of the routes relative to the app and the setup of the port. Express is also used for the app

The .env file contributes the following:

-Restores the DB username/password/and table, which enables access to the data base.

The connection.js file contributes the following:

-Establishes a connection to the database and connects the values from the .env file.

The package.json/package-lock.js contributes the following:

-Details on the dependencies for the project (mysq12, express, dotenv, and sequelize).

The seeds files contribute the following:

-The data for the relavant categories, i.e. shirts for category, cargo shorts as a product, 6 for product tag/tag, white for tag name.

The models files contribute the following:

-The addition of parameters for the data in each of the respective js files (Category, product, product tag, tab). See the below as an example from the category.js file.

      type: DataTypes.INTEGER,
      allowNull: false,
      primaryKey: true,
      autoIncrement: true

The routes files contribute the following:

-Applies the functions of the routes (get, put, post, delete).

## Usage

To jumpstart the application and setting up the code, you need to create the db in mysql (mysql -u root -p // source ./db/schema.sql). After that, the next step is to exit mysql and run the seeds in the commandline (npm run seed). And finally, to start the application, you need to enter npm start in the commandline and continue to Insomnia.

Please click the following link to view a step by step tutorial of the ecommerce backend database/command-line application in Insomnia.

[Demo](https://drive.google.com/file/d/1QI4LaDH0VDQ761pQ_PSg1PlZWuDfzvcX/view)

## Credits

Robert Patersons (Calendy Tutor) provided guidance on how to set up the folders and structure the requests in Insomnia.

## License

MIT License

Copyright (c) 2023 aubreymlj96

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
