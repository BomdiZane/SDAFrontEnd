# Introduction to Javascript

* Javascript is a *High level*, *interpreted* programming language
* It is not Java, but it shares similar programming constructs with Java and other C-like languages
* Javascript conforms to **ECMASCRIPT** specification. Other languages that follow same spec are JScript and ActionScript
* It is multi-paradigm => You can use OOP or Functional or both
* Runs on the client but also on the server via **Nodejs** engine


## Where is Javascript used?

* Most commonly used on web browsers 
	* Every browser implements a runtime engine for Javascript

	| Browser       | Engine        |
	| ------------- | ------------- |
	| Chrome        | V8            |
	| Firefox       | SpiderMonkey  |
	| Safari        | Nitro         |
	| Edge          | Chakra        |
	| Opera         | Carakan       |

* Build interactive user interfaces with libraries like ***React***
* Build full-stack applications with frameworks like ***Angular***, ***Next*** etc
* Build mobile applications with tools like ***ReactNative***, ***NativeScript***, ***Ionic*** etc
* Build desktop applications with tools like ***Electron***
* Build games with engines like ***Babylon***, ***Pixi***, ***Phaser*** etc 


## Types

Javascript has the following primitive types: 
* ***string***: Strings can be surrounded with double or single quotes
* ***number***: Integers and Decimals are both of type 'number' in Javascript, unlike in languages like C and Java which have separate *int* and *float*/*double* types
* ***boolean***: Booleans can either be *true* or *false* and are case sensitive
* ***undefined***: An undeclared or uninitialized variable is of type 'undefined'
* ***symbol***: Mostly used to avoid conflicts with object property keys. Introduced in es6. 

Functions are of type 'function'

Everything else is an object, including arrays, dates, regexp and null

NB: A single array can have values of different types and the array size is dynamic (you do not have to declare a size like in Java)


## Variables

Variables can be declared using the following keywords: 
* ***var***: 
	* Old syntax for declaring a variable
	* Has global scope which can lead to conflicts
	* Should be avoided

	```javascript
	var name;
	var age = 26;
	var isStaff = true;
	```
* ***let***: 
	* New syntax for declaring a variable
	* Introduced in es6 to solve problems with *var*
	* Has block scope

	```javascript
	let name = undefined;
	let age = null;
	let isStaff = true;
	let fruits = ['Apple', 'Orange', 'plum'];
	```
* ***const***: 
	* New syntax for declaring constants
	* Introduced in es6
	* Has block scope
	* Value cannot be changed once initialized

	```javascript
	// this will cause an error. Every constant must be initialized (assigned a value) upon declaration
	const name;
	const age = 32;
	const isStaff = false;
	const test = ['James', 5, null, undefined, true, {}];

	// NB: employee cannot be reassigned but its properties can still be modified
	const employee = { 
		name: 'John Doe',
		position: 'Full-stack Javascript Developer',
	};
	```

using undeclared variables will automatically create a global var declaration

```javascript
// employee has global scope
employee = {
	name: 'John Doe',
	position: 'Full-stack Javascript Developer',
};
```


## Comparisons

Comparisons in javascript are done using following:

* ***==*** 
	* This compares values but not types. 
	* It will attempt to do any possible implicit type conversions before the comparison

	```javascript
	5 == 5      // true
	5 == '5'    // true
	1 == true   // true
	0 == true   // false
	false == '' // true
	```

* ***===*** 
	* This compares values and types. 
	* No implicit type conversions are done before the comparison

	```javascript
	5 === 5      // true
	5 === '5'    // false
	1 === true   // false
	0 === true   // false
	false === '' // false
	```


## Author

Adombang Munang Mbomndih | [bomdisoft](https:bomdisoft.com)
