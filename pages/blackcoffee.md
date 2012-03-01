# BlackCoffee


##A flatiron http server template in coffee-script 
###based on [iron-coffee](https://github.com/twilson63/iron-coffee) 
by [Tom Wilson](https://github.com/twilson63/)

[Fork black-coffee on Github](https://github.com/gradus/black-coffee)

## Technologies
This is a template that can be used to create nodejs applications using 

* [Node v0.6.11](http://nodejs.org/)
* [Flatiron](http://flatironjs.org/)
* [CoffeeScript v1.2.0](http://coffeescript.org/)
* [CoffeeCup v0.3.5](https://github.com/gradus/coffeecup)
* [node-ecstatic](https://github.com/jesusabdullah/node-ecstatic)

---
## Getting Started

### Install [nodejs and npm](http://nodejs.org/)

    git clone http://github.com/gradus/black-coffee.git [project-name]
    cd [project-name]
    npm install .

This is just a template to get you started.

If you want to make this your own project on github:

    git remote rm origin
    git remote add origin git@github.com:[your github accountname]/[project-name].git


## Run

    node server.js

## About

[Black Coffee](https://github.com/gradus/black-coffee) is a template or boiler-plate to get started writing flatiron web applications in CoffeeScript.


 
It includes a Cakefile that lets you build, and watch your coffeescript as you develop.

Just hack away at app.coffee in the src directory.

The default CoffeeCup template for black-coffee is located in the pages directory.
Assets can be served from the 'assets' directory using [ecstatic](https://github.com/jesusabdullah/node-ecstatic).

#####Build

    cake build

#####Watch

    cake watch

#####Test
put your tests in the test directory

    cake test

###Example

[Enjoy your Coffee Black](http://black-coffee.jit.su).
   
---

## Thanks

* [Tom Wilson](https://github.com/twilson63) for creating iron-coffee
* [Jeremy Ashkenas](https://github.com/jashkenas) for creating coffee-script
* [Nodejitsu](https://github.com/nodejitsu) for creating flatiron

