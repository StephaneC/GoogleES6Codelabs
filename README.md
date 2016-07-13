![](https://cloud.githubusercontent.com/assets/110953/7877439/6a69d03e-0590-11e5-9fac-c614246606de.png)
## Codelab: Building your first ES2015 app

This repo contains the initial and final code for the [Building your first ES2015 app](http://www.code-labs.io/codelabs/chrome-es2015) codelab. (Not published yet! Working on it!)


# Class instead of prototypes
"much clearer and simpler way of defining classes"
That's right. People who came from Java wolrd will prefer this way. 

# Arrows instead of bind
"Arrow functions can be used in place of anonymous functions. The syntax is a lot shorter and less cumbersome"
--> Not sure about the lot shorter syntax.

# var
Let's use 'let' instead of var te declare variable. It reduces scope.

# Template String and interpolation
```javascript
StickyNote.TEMPLATE =
  '<div class="message"></div>' +
  '<div class="date"></div>' +
  '<button class="delete mdl-button mdl-js-button mdl-js-ripple-effect">' +
    'Delete' +
  '</button>';
```
  
  becomes
  
  ```javascript
  StickyNote.TEMPLATE = `
   <div class="message"></div>
   <div class="date"></div>
   <button class="delete mdl-button mdl-js-button mdl-js-ripple-effect">
     Delete
   </button>`;
```

```javascript
//ES5
this.dateElement.textContent = 'Created on ' + month + ' ' + date.getDate();
//ES6 way
this.dateElement.textContent = `Created on ${month} ${date.getDate()}`;
```

# Date formater
There is now a DateTimeFormat in ES6

# Spread


# Production ready? 
Babel.js  can transpil ES6 to es5
You can you for test purpose whith 
```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/babel-core/6.0.20/browser.min.js"></script>
```

For real deployment, use this instead (performance increased)
```shell
npm install babel-cli babel-preset-es2015 --save-dev
node_modules/.bin/babel --presets es2015 scripts/main.es6.js -o scripts/main.es5.js -s true 
```

