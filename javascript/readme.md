# JavaScript Style Guide

As a general rule, we've come to appreciate most of the style guidelines that Airbnb has established in their [JavaScript Style Guide](https://github.com/airbnb/javascript) and you should too.


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
var pulse-blaster;
function activate_pulse_cannon() { }

// good
var pulseBlaster;
function activatePulseCannon () { }

```