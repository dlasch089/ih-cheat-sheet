
# concepts
- module 2 project = backend rendered app (old school)
- http request/response cycle
- http headers & body
- http status codes
- data modelling
- nodejs (v8 in the backend)
- node modules & packages
- express & mongoose frameworks

# es6
- arrow functions have no context
- arrow functions usually as callbacks
- single line arrow functions (no brackets, implicit return)
- variables and constants
  - use const always
  - use let when const not possible
  - don't use var anymore
- es6 classes
- es6 with inheritance
- spread operator ...arr
- object shortcuts (implicit value)
- template (and multiline) strings

# nodejs
- runtime environment for running javascript in the backend (v8 engine)
- app can be an http server (runs "forever")
- runs javascript, same as browser (but no window, no DOM)
- start apps with "node app.js"
- node callbacks convection (err, result) => { ... }


# node modules
- every js file is a module
- every file has it's own scope (no global scope)
- npm packages are also modules
- for our files:
  - in mymodule.js do module.exports = ...
  - const mymodule = require('./folder/mymodule')
- for npm packages:
  - const express = require('express')

# npm
- http://npmjs.org
- npm init (new projects only)
- npm install (after cloning existing project)
- npm install --save package-name (add )
- npm install -g package-name (may require sudo)
- package.json (every node project needs one)
- always add "node_modules" to .gitignore

# package.json
- "scripts" are shortcuts
- "dependencies" are the packages the project needs to be executed
- "devDependencies" are the packages the developers need to work on the project

```
"scripts": {
  "start": "node app.js",
  "start-dev": "nodemon --inspect app.js"
}
```

# nodemon
- npm install -g nodemon
- nodemon --inspect app.js
- in package.json scripts
  - "start": "nodemon app.js"
  - "start-dev": "nodemon --inspect app.js"


# express generator
- npm install -g express-generator
- express my-project --view=ejs --git
- add start-dev to package.json scripts
- add launcher.json
- add .eslintrc.json (eslint --init) OR .jshintrc
- git init
- add .gitignore

# express
- http server framework
- pipeline of middlewares, followed by routes
- see snippets

# mongodb
- document database (as opposedd to relational database)
- stores data as documents, schema free, but relationships still exist
- instal mongodb, make sure it is running

# mongo shell
- $ mongo
- show dbs
- use databaseName
- db.help()
- show collections
- db.collectionName.help()
- db.collectionName.find().pretty()
- db.collectionName.insert({})

# mongo import
- mongoimport  --db databaseName  --collection collectionName --file fileName

# mongoose
- npm install --save mongoose
- object document mapper
- bring schemas into our use of mongodb
- see example schemas in `./snippets`
- types: String, Number, Date, Boolean, Array, Mixed, Objectid
