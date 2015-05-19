# JavaScript Style Guide

As a general rule, we've come to appreciate most of the style guidelines that Airbnb has established in their [JavaScript Style Guide](https://github.com/airbnb/javascript) and you should too.

Below you can find some quick hits for some of the most commonly questioned style guide items as well as any further custom items we've agreed on.


_more stuff to add here_


## Table of Contents

1. [Strings](#strings)
1. [Naming Conventions](#naming-conventions)
1. [Whitespace](#whitespace)



## Strings 

Use single quotes `''` for strings:

```javascript

// nope
var title = "Commander Space Cat";

// yep
var title = 'Commander Space Cat';

```


## Naming Conventions

Use camelCase for naming variables, objects, functions, and instances:

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

Use 2 spaces for indentation:

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

Use a single space before the leading curly brace:

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

Use a single space before the opening parenthesis in control statements (`if`, `while`, `for`, etc):

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

