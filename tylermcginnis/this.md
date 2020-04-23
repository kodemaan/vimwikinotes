### Implicit binding
This is usually what's to the left of the dot, odd example
```javascript
const user = {
  name: 'Tyler',
  age: 27,
  greet() {
    console.log(`Hello my name is ${this.name}`);
  },
  mother: {
    name: 'Stacey',
    greet() {
      console.log(`hello my name is ${this.name}`);
    }
  }
}

user.greet()
user.mother.greet()
```

### Explicit binding, call, apply, bind
bind it manually, either via function.call or .bind
call function binds to an object, and all subsequent arguments are passed
apply function does the same except it accepts an array of arguments
Example
```javascript
// call
const person = function(attribute) {
  console.log(`My name is ${this.name} and I am ${attribute}`);
}

const steve = {
  name: 'Steve'
}
person.call(steve, 'Cool') // My name is Steve and I am Cool
person.apply(steve, ['Cool']) // My name is Steve and I am Cool
const test = person.bind(steve, 'Cool')
test(); // My name is Steve and I am Cool
```

### New binding
Whenever function is invoked via the new keyword it's bound to the created object
```javascript
const person = function(name) {
  this.name = name;
}
const steve = new Person('Steve');
// This is now scoped to person function
```

### window binding
If no this is defined it defaults to the window or global object which is usually bad
```javascript
function test() {
  console.log(this.name);
}

test() // undefined
global.name = 'Steve'
test() // 'Steve'
```

[Back](/tylermcginnisnotes.md)
