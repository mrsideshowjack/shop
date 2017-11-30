# WEBRES SHOP

> live link [webres-shop](https://webres-7b761.firebaseapp.com/)

## Guidelines

Designing for users on the autistic spectrum

### Do
* use simple colours
* write in plain English
* use simple sentences and bullets
* make buttons descriptive - for example, Attach files
* build simple and consistent layouts
### Don't
* use bright contrasting colours
* use figures of speech and idioms
* create a wall of text
* make buttons vague and unpredictable - for example, Click here
* build complex and cluttered layouts

![poster](https://accessibility.blog.gov.uk/wp-content/uploads/sites/52/2016/09/autistic-spectrum.png)

### Setup

##### Prerequisites

Install [polymer-cli](https://github.com/Polymer/polymer-cli):

    npm install -g polymer-cli


##### Setup
    # Using CLI
    mkdir shop
    cd shop
    polymer init shop

    # Or cloning direct from GitHub
    git clone https://github.com/Polymer/shop.git
    cd shop
    bower install

### Start the development server

    polymer serve

### Run web-component-tester tests

    polymer test

### Build

Build presets provide an easy way to define common build configurations in your `polymer.json` file. There are 3 build presets we put in `polymer.json` file in Shop:

**es5-bundled**

- js: {minify: true, compile: true}
- css: {minify: true}
- html: {minify: true}
- bundle: true
- addServiceWorker: true
- addPushManifest: true
- insertPrefetchLinks: true

**es6-unbundled**

- js: {minify: true, compile: false}
- css: {minify: true}
- html: {minify: true}
- bundle: false
- addServiceWorker: true
- addPushManifest: true
- insertPrefetchLinks: true

**es6-bundled**

- js: {minify: true, compile: false}
- css: {minify: true}
- html: {minify: true}
- bundle: true
- addServiceWorker: true
- addPushManifest: true
- insertPrefetchLinks: true

Run the command to build the presets:

    polymer build

### Test the build

Use `polymer serve` to serve a specific build preset of the app. For example:

    polymer serve build/es5-bundled

## Deploy

##### Prerequisites

Install [firebase-tools](https://github.com/firebase/firebase-tools):

    npm install -g firebase-tools

##### Deploy
    polymer build
    firebase deploy