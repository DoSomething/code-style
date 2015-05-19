# JavaScript Style Guide

As a general rule, we've come to appreciate most of the style guidelines that Airbnb has established in their [JavaScript Style Guide](https://github.com/airbnb/javascript) and you should too.

Below you can find some quick hits for some of the most commonly questioned style guide items as well as any further custom items we've agreed on.


_more stuff to add here_


## Table of Contents

1. [Strings](#strings)
1. [Naming Conventions](#naming-conventions)
1. [Whitespace](#whitespace)
1. [Comments](#comments)



## Strings 

Use single quotes `''` for strings.

```javascript

// nope
var title = "Commander Space Cat";

// yep
var title = 'Commander Space Cat';

```


## Naming Conventions

Use camelCase for naming variables, objects, functions, and instances.

```javascript

// nope
var pulse_blaster;
function activate_pulse_cannon() { }

// yep
var pulseBlaster;
function activatePulseCannon() { }

```


## Whitespace

DoSomething.org projects typically include an [Editor Config](http://editorconfig.org/) file to help enforce editor settings across code editors.

Use 2 spaces for indentation.

```javascript

// nope
function() {
••••var spaceLitter;
}

function() {
•var spaceLitter;
}

// yep
function() {
••var spaceLitter;
}

```

Use a single space before the leading curly brace.

```javascript

// nope 
function spaceCatFancier(){
  console.log('accepted human');
}

// yep
function spaceCatFancier() {
 console.log('accepted human'); 
}

```

Use a single space before the opening parenthesis in control statements (`if`, `while`, `for`, etc).

```javascript

// nope 
if(isSpaceMouse) {
  catchNemesis();
}

// yep
if (isSpaceMouse) {
  catchNemesis();
}

```

Do not use any spaces before the argument list in function calls and declarations.

```javascript

// nope
function catchNemesis () {
  console.log('use laser mouse trap');
}

// yep
function catchNemesis() {
  console.log('use laser mouse trap');
}

```

Use spaces between operators and operands.

```javascript

// nope
var laserEyes=x*2;

// yep
var laserEyes = x * 2;

```


## Comments

Use `/** ... */` for multi-line comments. Include a description, define the parameters (specify the types within curly braces and title case) and return values.
Use an empty commented out line between the description and parameter definitions.

```javascript

// nope
// Executes a method to catch one of the fiesty villainous Space Mice based on 
// the name of the Space Mouse provided
//
// @param {String} name
// @return {Object} spaceMouse
function catchNemesis(name) {
  
  // ... do something to catch space mouse ...
  
  return spaceMouse;
}


// yep
/**
 * Executes a method to catch one of the fiesty villainous Space Mice based on 
 * the name of the Space Mouse provided
 *
 * @param {String} name
 * @return {Object} spaceMouse
 */
function catchNemesis(name) {
  
  // ... do something to catch space mouse ...
  
  return spaceMouse;
}

```
