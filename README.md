#NodeJS Music Band Showcase#

##Requires##
- NodeJS for server running
- MYSQL for database
- sequelize for database schema & migration
- swig for HTML templating

##Usage##
1. run `npm install -g mysql` to install mysql
2. run `npm install -g sequelize-cli` to install [sequelize-cli](https://github.com/sequelize/cli)
3. run `npm install` to install packages locally
4. open 'mysql.exe' in '..\mysql\bin' (or run `mysql-ctl cli` to go into mysql cli if you use c9.io)
5. run `sudo mysql` (or `mysql -u youruser -p yourpassword`) to sigin sql
6. create a new database `CREATE DATABASE mvc_mysql_app;` then `Ctr + C` to exit mysql
7. reconfig './config/config.json' file.
8. `sudo sequelize db:migrate --migrations-path config/migrations` to insert data on Mysql
9. signin to mysql (like step #5), run `use mvc_mysql_app;` then run `show tables;` to show tables which we migrated (or use [sequelpro](http://www.sequelpro.com/) for that
10. run `source mvc_mysql_app.sql` to import database from 'mvc_mysql_app.sql' file; then press 'Ctr + C'
10. run `npm start` to start server

##References##
1. Mysql on c9.io
 - https://docs.c9.io/docs/setup-a-database
 - https://community.c9.io/t/setting-up-mysql/1718
 - http://stackoverflow.com/questions/27931929/c9-io-how-to-find-the-host-address-to-make-a-mysql-connection-in-node-js-platf
2. Using sequelize
``` shell
> sequelize init
# will generate "config/config.json", "/config/migrations", "/models" folders
> sequelize model:create --name User --attributes "name:string, email:string"
# will generate "models/User.js"
> sequelize model:create --name Band --attributes "name:string, description:string, album:string, year:string, UserId:integer"
# will generate "models/Band.js"
```