# ES6 Classes - Currency Project

## Description

This project explores **ES6 classes** in JavaScript. It covers defining classes, adding methods, extending classes, and leveraging advanced features such as static methods and metaprogramming with symbols. The key component of the project is a `Currency` class that manages currency details.

## Learning Objectives

By the end of this project, you will be able to:

### 1. How to Define a Class

A class is a blueprint for creating objects. In ES6, you can define a class using the `class` keyword:

```javascript
class Currency {
  constructor(code, name) {
    this._code = code;
    this._name = name;
  }
}

2. How to Add Methods to a Class
Methods can be added to a class by defining functions inside the class body:

class Currency {
  constructor(code, name) {
    this._code = code;
    this._name = name;
  }

  displayFullCurrency() {
    return `${this._name} (${this._code})`;
  }
}

The displayFullCurrency() method is added to the Currency class, which formats and returns the currency information.

3. Why and How to Add a Static Method to a Class
Static methods are functions that belong to the class itself rather than to instances of the class. They are useful when the method doesn't require any instance-specific data. You declare static methods using the static keyword:
class Currency {
  // Other methods and constructor

  static compare(currency1, currency2) {
    return currency1._code === currency2._code;
  }
}
Here, compare() is a static method that compares two currencies based on their code.

4. How to Extend a Class from Another
In JavaScript, classes can inherit properties and methods from other classes using the extends keyword:
class CryptoCurrency extends Currency {
  constructor(code, name, blockchain) {
    super(code, name);
    this._blockchain = blockchain;
  }
}
The CryptoCurrency class extends the Currency class, inheriting its properties and methods. The super() method calls the parent class constructor.

5. Metaprogramming and Symbols
Symbols in JavaScript are unique and immutable data types that can be used as keys for object properties, enabling you to create "hidden" properties or for metaprogramming:

const uniqueKey = Symbol('uniqueKey');

class Currency {
  constructor(code, name) {
    this[uniqueKey] = code;
    this._name = name;
  }
}
Here, uniqueKey is a Symbol used as a key for the Currency class, ensuring that the property is hidden and cannot be easily accessed.

Usage
Example usage of the Currency class:
const usd = new Currency('USD', 'United States Dollar');
console.log(usd.displayFullCurrency()); // Output: United States Dollar (USD)

Author
Ilyas Ettourach
