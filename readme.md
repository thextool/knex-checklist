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
- [ ] express --git . (creates a git ignore. If you don't have this already type $ npm install -g express generator)
- [ ] you will only need to do npm install and can skip down to 
- [ ] npm start
- [ ] touch .gitignore
- [ ] npm init -y (this creates a package.json file)
- [ ] Create GitHub repo
- [ ] Link to GitHub repo
- [ ] Create Heroku Dyno
- [ ] Set Heroku buildpack to nodejs. this is under settings
- [ ] Link to Heroku Dyno. on deploy page copy paste the url at the bottom to my local repo.
- [ ] npm install - if dependencies aren't already there do the following. 
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
- [ ] Update client and connection in knexfile.js for development client use
      client: 'pg',
      connection:'postgres://localhost:/[database name]'
- [ ] for production use (this is telling heroku what database to use in produciton
      client: 'pg',
      connection: process.env.DATABASE_URL
- [ ] knex migrate:make [choose a name]
- [ ] knex seed:make [choose a name]
- [ ] git commit
- [ ] in the knexfile.js write the schemas to create the table and it's colums. looks something like this 
      ```return knex.schema.createTable('resolutions', (table) => {
        table.increments('id')
        table.date('dueDate').notNullable()
        table.text('resolution').notNullable()```
    })
 - [ ] $ knex migrate:latest - this will create the table and the columns. 
 - [ ] you can check and see if it worked by psql [dbname] 
 - [ ] \dt describe table 
 - [ ] \d [table name]
 - [ ] leave the db with \q
 - [ ] heroku addons:create heroku-postgresql
 - [ ] git add commit push
 - [ ] git push heroku master
 - [ ] heroku run knex migrate:latest
 





## Now All Files Are Set Up To Begin Crushing Some Code

### Files to edit

_Sorry. The following checklist includes hints only_

- [ ] Edit database-connection.js with proper port
- [ ] Edit knex up/down in the migrations file
- [ ] Add data from drill README.md to the seed file
