# JavaScript Style Guide

As a general rule, we've come to appreciate most of the style guidelines that Airbnb has established in their [JavaScript Style Guide](https://github.com/airbnb/javascript) and you should too.

Below you can find some quick hits for some of the most commonly questioned style guide items as well as any further custom items we've agreed on.


_more stuff to add here_


## Table of Contents

1. [Strings](#strings)
1. [Naming Conventions](#naming-conventions)



## Strings 

Use single quotes `''` for strings:

```javascript

// bad
var title = "Commander Space Cat";

// good
var title = 'Commander Space Cat';

```


## Naming Conventions

Use camelCase for naming variables, objects, functions, and instances:

```javascript

// bad
var pulse_blaster;
function activate_pulse_cannon() { }

// good
var pulseBlaster;
function activatePulseCannon() { }

```


## Whitespace

DoSomething.org projects typically include an [Editor Config](http://editorconfig.org/) file to help enforce editor settings across code editors.

Use 2 spaces for indentation:

```javascript

// bad
function() {
••••var spaceLitter;
}

function() {
•var spaceLitter;
}

// good
function() {
••var spaceLitter;
}

```

Use a single space before the leading curly brace:

```javascript

// bad 
function spaceCatFancier(){
  console.log('accepted human');
}

// good
function spaceCatFancier() {
 console.log('accepted human'); 
}

```

Use a single space before the opening parenthesis in control statements (`if`, `while`, `for`, etc):

```javascript

// bad 
if(isSpaceMouse) {
  catchNemesis();
}

// good
if (isSpaceMouse) {
  catchNemesis();
}

```

