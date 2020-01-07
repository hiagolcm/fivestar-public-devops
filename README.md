# Fivestar Deploy

## Artifacts

To deploy the application the following artifacts will be needed:

- MySQL Database dump
- App source code

Contact hcardealdemelo@gmail.com to get access to both of them

## Domain Setup

Contact hcardealdemelo@gmail.com to redirect the production domain to your server IP.

## Server Setup

The following applications must be installed in you environment:

- MySQL or MariaDB
- [Yarn](https://github.com/yarnpkg/yarn)
- Node

## MySQL/MariaDB config

Create a database called `fivestar`. Then create an user called `fivestar` with password `fivestar`. For example:


sudo mysql -u root
CREATE USER 'fivestar'@'localhost' IDENTIFIED BY 'fivestar';
GRANT ALL PRIVILEGES ON fivestar.* TO 'fivestar'@'localhost';


After this, use the provided dump in the `fivestar` database. For example:


sudo mysql --user root --database=fivestar < fivestar.sql


## Build

In the source code folder run the command `yarn build`. Then `/build` will be created.

## Run Application

Use node to run the application: `node build/index.js`

This application uses the port `3000`. You will need to use an application like Nginx in order to map the port 80 from your server to the port `3000`.
