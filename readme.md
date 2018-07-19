# Knex Checklist

_NOTE: This is specifically for the Galvanize Knex Drills. If you haven't done so already, please visit the link below to fork and clone the Knex drill repo (galvanize-memory) before you begin_

[Galvanize Memory](https://github.com/gSchool/galvanize-memory)

## If You Have Not Installed a Database Language

### 1: Install on Mac with Homebrew with one of the following database options

- [ ] brew install postgresql
- [ ] brew install mysql
- [ ] brew install mariadb

### 2: Start your database

_NOTE: Even if you have installed a database and done a million database drills, ALWAYS begin with the following command to check everything is up and running_

- [ ] brew services start postgresql

- Above command should either successfully start or say already started

### 3: Now the fun begins

- [ ] Create new directory outside the cloned Knex repo
- [ ] Copy repo drill files into new directory (using cp -r)
- [ ] git init
- [ ] touch .gitignore
- [ ] npm init
- [ ] Create GitHub repo
- [ ] Link to GitHub repo
- [ ] Create Heroku Dyno
- [ ] Link to Heroku Dyno
- [ ] Set Heroku buildpack to nodejs
- [ ] npm install
- [ ] npm install pg
- [ ] npm install knex
- [ ] npm install cors
- [ ] npm install express
- [ ] npm install morgan
- [ ] git commit
- [ ] createdb 'dbname'
- [ ] psql 'dbname' (check database has been created)
- [ ] Add knex and start scripts to package.json
- [ ] knex init
- [ ] Update client and connection in knexfile.js
- [ ] knex migrate:make game
- [ ] knex seed:make game
- [ ] git commit

## Now All Files Are Set Up To Begin Crushing Some Code!

### Knex Migration File

- [ ] Edit database-connection.js with proper port
- [ ] Edit knex up/down in the migrations file
- [ ] Add data from drill README.md to the seed file
