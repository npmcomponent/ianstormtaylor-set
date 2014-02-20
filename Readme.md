*This repository is a mirror of the [component](http://component.io) module [ianstormtaylor/set](http://github.com/ianstormtaylor/set). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/ianstormtaylor-set`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*
# set

  Set a property on a model or object. For the reverse, checkout [`ianstormtaylor/get`](https://github.com/ianstormtaylor/get).

## Installation

    $ component install ianstormtaylor/set

## Example

Plain objects:    
```js
var set = require('set');

var person = { name: 'ulysses' };
set(person, 'name', 'achilles');
person.name; // achilles
```

Getter/setter methods:
```js
var set = require('set')
  , model = require('model');

var Person = model('person').attr('name');
var person = new Person({ name: 'ulysses' });
set(person, 'name' 'achilles'); 
person.name(); // achilles
```

Get methods:
```js
var Backbone = require('backbone')
  , set = require('set');

var person = new Backbone.Model({ name: 'ulysses' });
set(person, 'name', 'achilles')); 
person.get('name'); // achilles
```

## API

### set(model, prop, value)
  Get the `model`'s `prop` to` `value`.

## License

  MIT
