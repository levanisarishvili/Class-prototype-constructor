```javascript
// With Constructor
function CarFun(name) {
  this.name = name

  this.getName = function() {
    
    console.log(this.name)
  }
}


// With prototype
function CarFunProp(name) {
  this.name = name
}

CarFunProp.prototype.getName = function() {
  console.log(this.name)
}

class CarWithClass {
  constructor(name) {
    this.name = name
  }

  getName() {
    console.log(this.name)
  }
}

// Constructor
const constructorCar = new CarFun('BMW')
constructorCar.getName()

// Prototype
const prototypalCar = new CarFunProp('Ford')
prototypalCar.getName()

// Class (ES6)
const classCar = new CarWithClass('Mercedes')
classCar.getName()


// Curring
var add = function (a){
 return function(b){
   return function(c){
      console.log(a+b+c)
    }
  }
}

const addNumberTo10 = add(5)(5)
addNumberTo10(20)
addNumberTo10(100)


```
