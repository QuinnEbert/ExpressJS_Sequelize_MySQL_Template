ExpressJS_Sequelize_MySQL_Template
==================================

Bare minimal ExpressJS+Sequelize+MySQL project, code managed by NodeJS

Features
--------

This is basically the result of the "Use with Express" Sequelize tutorial, minus their full example code, with the proper mods made to `bin/www`.

* Dependencies managed with NodeJS
* ExpressJS framework
* Sequelize framework
* Ready to use with MySQL databases via Sequelize (dependencies included!)

Purpose
-------

This gives me an easy starting point for other, future projects, so I needn't waste time on setting up the basics.  :)

Objective
---------

After running the Setup steps (below) you should be able to set straight off coding for MySQL/SequelizeJS.  I have modified the default generated project so it will, indeed, auto-sync the database (create the tables and whatnot) at startup assuming you configured the DB stuff properly.

Setup
-----

1. Clone the repo.
2. Update all the DB server info in `config/config.json`.
3. Run `npm install` from within the local repo copy.
4. Within the local repo copy run `./bin/www` if the server didn't auto-start after `npm install`.
5. Access `http://<your_development_server_ip>:3000` to see the app server running!
