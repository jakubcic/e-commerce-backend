# E-Commerce Back End
[![MIT License badge](https://img.shields.io/badge/license-MIT-yellow.svg)](https://choosealicense.com/licenses/mit/)

## Table of Contents

- [Description](#description)
- [Installation](#installation)
    + [Prerequisites](#prerequisites)
    + [How to install](#how-to-install)
- [Usage](#usage)
- [Credits](#credits)
- [License](#license)


## Description
This is an e-commerce back end built with Express.js and a MySQL database. The API exposes the following endpoints and supports the listed HTTP methods:

| Endpoint              | Supported Methods |
|-----------------------|-------------------|
| `/api/categories`     | GET, POST         |
| `/api/categories/:id` | GET, PUT, DELETE  |
| `/api/tags`           | GET, POST         |
| `/api/tags/:id`       | GET, PUT, DELETE  |
| `/api/products`       | GET, POST         |
| `/api/products/:id`   | GET, PUT, DELETE  |
<br>

## Installation
### Prerequisites
If you want to run this application locally, you must have **node.js** installed. I highly recommend using [**nvm**](https://github.com/nvm-sh/nvm) (node version manager) to manage your node.js installation.
<br>
This application is based on **node v16.18.1**.
You must also have a local MySQL server installed. You can [use homebrew to install it on macOS](https://formulae.brew.sh/formula/mysql#default). Install homebrew if you don't have it already, then in a terminal run the following:
```
brew install mysql
```
Check if your MySQL server is running:
```
brew services info mysql
```
If not, run:
```
brew services start mysql
```
Next, secure your MySQL server with a root password and other recommended settings by running:
```
mysql_secure_installation
```


### How to install
After you ensure that you have **node.js** and **MySQL** installed you can simply clone this repositry:
```
git clone git@github.com:jakubcic/e-commerce-backend.git
```

Then in your terminal navigate to the root of the **e-commerce-backend** directory and run:
```
npm install
```

## Usage
Once you have everything installed, including the dependencies, you must create the database schema. You can use the default `mysql` shell that comes pre-installed with the **MySQL** package or a third party MySQL CLI client like [mycli](https://github.com/dbcli/mycli) which is my preference. Hooray for tab-completion and syntax highlighting! Once you're connected to the **MySQL** server with whatever method you choose, run the following:
```
source db/schema.sql
```
This will create the database schema. Note that you must start the **MySQL** shell from within the **e-commerce-backend** directory for this path (`db/schema.sql`) to work.

Next we'll seed the database. In our **package.json** we've configured a few scripts. One of them is `seed`. You can run the following to call the seed script **seeds/index.js**:
```
npm run seed
```
Now that we're set up with the database we can run the server (and start calling the API endpoints!). 
```
npm run start
```
<br>

Here's a video demo showcasing all the possible API calls:

https://user-images.githubusercontent.com/39972418/208597878-28dadb87-2db4-4bfe-a7f0-169bd1539aba.mp4


## Credits
### Dependencies
This application uses v4.17.1 of [express.js](https://www.npmjs.com/package/express), v2.1.0 of the [mysql2](https://www.npmjs.com/package/mysql2) package, and v6.27.0 of [sequelize](https://www.npmjs.com/package/sequelize). 

## License
This application is covered under the [MIT License](https://choosealicense.com/licenses/mit/).


