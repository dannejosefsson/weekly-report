# Vagrant and Puppet configuration for NodeJS & MongoDB.

Vagrant configuration with puppet to create a Virtual Box machine with Ubuntu Server 14.04.

Installation:
Install Vagrant on your machine.
Install Virtual Box on your machine.

Puppet Manifest will install:
[Nodejs v0.10.\*, MongoDB 2.4.\*, wget, git, vim, htop]

## How to get started

SSH into vagrant, cd /vagrant/app , run `npm install` to grab the dependencies, and start hacking!

### Running the app

Runs like a typical express app:

    node app.js

## Directory Layout /vagrant/app/*

    app.js              --> app config
    package.json        --> for npm
    public/             --> all of the files to be used in on the client side
      css/              --> css files
        app.css         --> default stylesheet
      img/              --> image files
      js/               --> javascript files
        app.js          --> declare top-level app module
        controllers.js  --> application controllers
        directives.js   --> custom angular directives
        filters.js      --> custom angular filters
        services.js     --> custom angular services
        lib/            --> angular and 3rd party JavaScript libraries
          angular/
            angular.js            --> the latest angular js
            angular.min.js        --> the latest minified angular js
            angular-*.js          --> angular add-on modules
            version.txt           --> version number
    routes/
      api.js            --> route for serving JSON
      index.js          --> route for serving HTML pages and partials
    views/
      index.jade        --> main page for app
      layout.jade       --> doctype, title, head boilerplate
      partials/         --> angular view partials (partial jade templates)
        partial1.jade
        partial2.jade

## Example App

A simple [blog](https://github.com/btford/angular-express-blog) based on this seed.

## Contact

For more information on AngularJS please check out http://angularjs.org/
For more on Express and Jade, http://expressjs.com/ and http://jade-lang.com/ are
your friends.