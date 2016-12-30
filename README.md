#NodeJS Music Band Showcase#

##Requires##
- NodeJS for server running
- MYSQL for database
- sequelize for database schema & migration

##Usage##
1. run `npm install -g mysql` to install mysql
2. run `npm install -g sequelize-cli` to install [sequelize-cli](https://github.com/sequelize/cli)
3. run `npm install` to install packages locally
4. open 'mysql.exe' in '..\mysql\bin' (or run `mysql-ctl cli` to go into mysql cli if you use c9.io)
5. run `sudo mysql` (or `mysql -u youruser -p yourpassword`) to sigin sql
6. create a new database `CREATE DATABASE mvc_mysql_app;` then `Ctr + C` to exit mysql
7. `sudo sequelize db:migrate --migrations-path config/migrations` to insert data on Mysql
8. signin to mysql (like step #5), run `use mvc_mysql_app;` then run `show tables;` to show tables which we migrated
9. run `npm start` to start server

##References##
- For c9.io
-- https://docs.c9.io/docs/setup-a-database
-- https://community.c9.io/t/setting-up-mysql/1718
-- http://stackoverflow.com/questions/27931929/c9-io-how-to-find-the-host-address-to-make-a-mysql-connection-in-node-js-platf