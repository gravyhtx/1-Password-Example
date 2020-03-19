# 1-Password Example


## User Story

```md
*AS A* web developer
*I WANT* royalty-free code that can demonstrate an encrypted password verification
*SO THAT I* can use it in any of my projects
```


## Function

This is an application to store and authenticate emails and passwords for your website. This is only a demo for running on your local server using Express so do not complain if this doesn't work on your website until after you have thoroughly researched online deployment for server based websites with a MySQL database. For easy deployment using JawsDB for Heroku, visit https://devcenter.heroku.com/articles/jawsdb. Oh, and read this README... I didn't just do this for fun.



## Installation

In order to get this program to work on you systems, you must install the following dependencies in the root folder (same file level as the ‘server.js’ file) wherever this folder is located. All dependencies listed in the 'package.json' file include the following.

```json
"dependencies": {
    "express": "^4.17.1",
    "mysql": "^2.18.1",
    "mysql2": "^2.1.0",
    "sequelize": "^5.21.5"
  }
```


Install these dependencies with npm, navigate to this folder in your console terminal and enter the following command.

```zsh
$ npm i bcryptjs express express-session mysql2 passport passport-local sequelize
```


Ensure you have installed dependencies by turning on the option to show hidden files in your file system and checking that a 'package-lock.json' file and a 'node_modules folder' is created. You can positively verify dependencies are installed by opening the 'package-lock.json' file and see that all dependencies listed above are in this file. 



For documentation on npm please visit https://docs.npmjs.com/



## Operation

Before operating this program you must first install Node.JS (6.14x or greater) and MySQL Workbench.


### Node.JS

Check your current version type the following command in your console terminal.

```zsh
$ node -v
```


You can install the latest package from https://nodejs.org/en/download


or if you are using homebrew

```zsh
$ brew install node
```



### MySQL Workbench

Install the latest version:

https://dev.mysql.com/downloads/workbench/

Documentation can be found at https://dev.mysql.com/doc/workbench/en/


Open MySQL Workbench and create a new schema on default route http://localhost:8080/ by typing:

```sql
CREATE DATABASE passport_demo;
```


Run this command by clicking the lightning bolt button to run and verify database is created by clicking the refresh button on the top right of the <b>SCHEMAS</b> list.

Finally, go into the 'config.json' file (found in the 'config' folder) and type your MySQL password into the development, test, and production 'password' objects.



### Deployment

Once current Node.js version is verified and 'passport_demo' database is created, you can navigate to the root folder of this program in your console terminal and run the following command.

```zsh
$ node server.js
```


If this program is running properly you will see a success message in your console terminal:
```
==> 🌎  Listening on port 8080. Visit http://localhost:8080/ in your browser.
```


This program will run in your browser at http://localhost:8080/

If you're unable to run this program because of an error message:

* Be sure you've verified you're in the correct folder in your console terminal
* Make sure the 'passport_demo' database is listed in 'SCHEMAS' list in MySQL
* Check that all dependencies are installed (which will be found in console terminal error log with modules not found)

Otherwise you may need to install all program contents again.


Password is securely encrypted using bycrypt password hashing and authenticated by Passport.js middleware for Node.js.



## Bugs

For a list of known bugs plese visit documentation for this program's dependencies.