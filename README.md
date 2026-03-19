# javascript
Node js allows developers to write JavaScript code that runs directly in a computer like in vs codes terminal itself instead of in a browser. There are also other js environment other than node.js like deno.js etc
node is an compiler made by chrome's javascript engine that is v8 engine + some c++ code.
every browser has different js engine for runing js code.
Node js helps in executing the js file and dispalys the output
If we don't install node.js then we cant run js file in vs code's terminal.
node -v command is used for checking the version of node.js or to check whether node is installed or not.
node filename.js to execute js file.

console.log() - is used for printing.
console.table(data,columns) : used to show data in table format.
data : array or object
columns : it is optional. But it should be array containing the columns which you want in your table.
some other console methods : 
assert()
clear()
count()
countReset()
error()
group()
groupCollapsed()
groupEnd()
time()
timeEnd()
timeLog()
trace()
warn() etc.
// is used for single line comment.
/* */ is used for multi line comment's.
At the end of the line you can use semicolumn(;) or you can ignore using it.
prompt(message(optional)): pops up a input box and converts input value into string.
alert(message): pops up a alert box.

variables in js :
A variable is a name given to a memory location in a computer’s memory. It is used to store data that can be changed during program execution.
constant(const) : constant variables value cannot be changed after assigning a value to it.
	               variables created by const keyword cannot be redeclared and reassigned.
    	          But we can update the values of array or object,like adding new element to array or key to object.
				  in short, the space is fixed not the value in the space.
example : const myName = "abhishek" 
          myName="abhi" // error
let : variables created by let keyword cannot be redeclared in the same scope, but we can reassign the value of the variable.
example : let myName = "abhishek"
           myName="abhi" // no error
var :  var is not used commonly because of it's issue in block scope and functional scope. var was widely used in older version's of javascript.
	   variables created by var keyword can be redeclared and we can reassign the value of the variable.
nothing : No keyword is used for defining a variable here.
Example :  myName="abhi" // no error
good practice : use const more instead of let.
Scope :
    let and  const variables are block scope. That means variables are only available inside a block not outside the block.
    var variables are global scope. That means variables are available throughout the code.
	
identifiers : identifier is a name given to variable by following some rules.
			  1. we can use uppercase and lowercase alphabets.
			  2. we can use numbers from 0-9.
			  3. we can only use underscore(_) and dolloar($) sign's only.
			  4. variable name should start with alphabet or underscore(_) or dolloar($) only, not with number.
			  5. variable name cannot be a keyword like while,for,if,function etc.
			  6. JavaScript is case sensitive, that means A and a are different.

Data Types:
  
7  Primitive Datatypes:
	
Null : 	It's value is nothing.
Example : let a = null 

Undefined : It is nothing but not assigning a value to a variable after creating it or declaring it.
Example : let a 
	  console.log(a) // undefined
	
Boolean	 : It has two values true and false.
Example : let ans = true or false
	
Number : Both integers and float values come under Number datatype.
Example : let a = 10
	  let b = 11.1
	
BigInt : It is used to very large integer values.
Example : let a = 99999n
put n at the end of the number, so it will become Big integer.
	
String : It is collection of characters enclosed in single or double quotes and it is immutable.
Example : let name = "Abhishek"
string+string = string
string+number=string
except +, all other operators like -,*,/,%,** result in number with string
In js, + behaves differently with string, that means it converts the other operand into string.
whereas other operators, try to convert the string into number.
ex : 'abhi'+'shek'='abhishek'
     'abhi'+4 = 'abhi4'
     '123'+4 = '1234'
     'abhi'- 4 = NaN
     '123' -3= 120
Symbol	: It is used for making a value or anything as unique and it is immutable.(not a correct definition)
		  in future while using symbol, use toString() method with it.
Example : let a = Symbol(10)
	  let b = Symbol(10)
	  log(a === b) // false because == checks only values but === checks value and datatype, here both values are considered as unique


Type Conversion :

let a = Number("10") // string to number 10
let b = String(10) // "10"
let c = BigInt(10) // 10n
let d = Boolean(1) // 1 is nothing but true
let e = Null()
let f = Undefined()
let g = Symbol()
typeof() is used return the type of the variable or value.

NaN : It stands for not a number
two NaN's cannot be same.so use Number.isNaN() method.

Typeof	        typeof return value	

Null	           "object"	( its an bug from 1995, it should be null, but it returns object)
Undefined	 	  "undefined"	
Boolean	          "boolean"	
Number	           "number"	
BigInt	           "bigint"	
String	           "string"	
Symbol	           "symbol"
array              "object"
object             "object"
function           "function"

100000 can be written as 1_00_000, it's just a syntactic sugar or a way of writing in js.

e stands for 10
ex : 2e2 // 2*10^2 == 2*100 == 200
ex : 2e-2 // 2*10^(-2) == 2/100 == 0.02

octal number : base 8 and numbers from 0 to 7
ex : 0o2

hexadecimal number : base 16 and numbers from 0 to 15 ( 10 to 15 are represented from A to F)
ex : 0x123f

binary number : base 2 and numbers from 0 to 1
ex : 0b111


In JavaScript, non-primitive values are stored and copied by reference (pointer to address ).
When you assign or pass them, the reference (memory address) is copied, not the actual object.

Non Primitive Datatypes : Arrays, objects, functions etc // Non Primitive Datatypes are passed as reference that means if we change value of one variable the value also gets changed in another variable unlike primitive datatypes . example : let a = 10
				let b = a // b = 10
    				b = 9 // here b value changes but a value doesn't change 
				let a = [1,2,3]
    				let b = a // b = [1,2,3], b and a point to [1,2,3]
				b.push(4) // b array changes and a array also changes because a and b point to same array 
shallow copy : it only copies values, but the reference or address is same.
To overcome this, we use spread operator(...) for copying arrays, objects etc or using Object.assign().
But, nested objects are still shared.
deep copy : it copies values and the reference or address is different.
use structuredClone() or JSON.parse(JSON.stringify()) methods.


Backticks : ` `
example : let name = "abhi"
	  let age = 22
	  console.log(` my name is ${name} and I am ${age} years old `) // instead of "my name is" + name + "and I am" +age+ "years old"

escaping character is \ this backslash escapes the next character.
ex : "my name is \"abhishek\" "
o/p : my name is "abhishek"

if we use template literal ( ` ` ), the way we write the string, the output string is also same and no need to use \n, \t etc special characters in template literal. 

naming convension : pascal case : first letter of every word should be capital. example : Abhishek or AbhishekBiradar // this convension is used for class names
camel case : except first word, first letter of other words should be capital example : abhishek or abhishekBiradar // this convension is used for variables,method names etc
Constants are often in UPPERCASE.
Example : MAX_VALUE
These conventions, are not mandatory rules, but following them makes code easier to read and understand.

// object in js are different from objects in other languages.
 object in js
 ex : let obj = { key : value } 
 objects in js also have properties and methods.

String :
string in js are immutable. That means we cannot do :
Example - let a ="abhi"
          a[0] = "A" // error
But we can reassign a new string value to the variable.
Example : let a ="abhi"
		  a="abhishek"
	      a[99] // gives undefined
		  a.charAt(99) // gives empty string
		  a.at(99) // gives undefined
new keyword is used create an object 
let name1 = "abhi" // typeof name1 is string
let name = String("abhi") // typeof name is string
let name2 = new String ("abhishek")  // typeof name2 is object // internally name2 = { }
Few string properties : length
Few string methods : 
at() : it returns a new string by extracting the character from a specified index of other string.
		it also works with negative indexing.(-1 represents last character of a string)
		ex : name.at(-1) // i
chartAt() : it returns a new string by extracting the character from a specified index of other string.
		    it does not work with negative indexing.
			ex : name.charAt(0) // a
concat() : it returns a new string by adding two strings.
		   ex : let a = name.concat("shek")
startsWith(), endsWith() : true or false
toUpperCase(), toLowerCase()
includes() : returns true or false, if the string is present or not in the string.
			 ex : let myName = "abhishekbiradar"
			 	  console.log(myName.includes("abhi")) // true
indexOf() : searches the string and returns the index of the first occurrence of the specified substring. return value : index or -1.
lastIndexOf() : searches the string and returns the index of the last occurrence of the specified substring. return value : index or -1.
padStart(finalstringlength,value) : pads this string with a given string ,so that the resulting string has a given length. The padding is applied from the start of this string.
padEnd(finalstringlength,value) : pads this string with a given string ,so that the resulting string has a given length. The padding is applied from the end of this string.
repeat(count) : returns a new string which contains the specified number of copies of the string.
replace(oldtext, newtext) : returns a new string, only the first occurrence will be replaced. The original string is left unchanged.
replaceAll(oldtext, newtext) : returns a new string, all occurrence's will be replaced. The original string is left unchanged.
slice(indexStart) or slice(indexStart, indexEnd-1) : it returns a new string by extracting a portion from the original string.
split() : split's the string by using the separator and returns an array of strings.
substring() : it returns a new string by extracting a portion from the original string.
Feature	                          slice()	substring()
Negative values	                    Yes	       No
Swaps start & end if start > end	No	       Yes
Works on arrays	                    Yes	       No (string only)
toString() : returns a new string by converting the given input into string.
trim() : removes whitespace's from both ends of this string and returns a new string, without modifying the original string.
trimStart() : removes whitespace's from starting of the string and returns a new string, without modifying the original string.
trimEnd() : removes whitespace's from ending of the string and returns a new string, without modifying the original string.
match()
search()
etc

Number :

let num = new Number(10) // typeof num is object not number
number properties : 

EPSILON
MAX_SAFE_INTEGER
MAX_VALUE
MIN_SAFE_INTEGER
MIN_VALUE
NaN
NEGATIVE_INFINITY
POSITIVE_INFINITY

number methods : 

Number.isFinite() : it checks that a given value is a finite number or not.( true or false )
Number.isInteger() : it checks that a given value is a integer or not.( true or false )
Number.isNaN() : it checks that a given value is a NaN or not.( true or false )
Number.isSafeInteger() : checks, whether the integer is between -(2 power 53 – 1) and (2 power 53 – 1).( true or false )
Number.parseFloat() : converts a string into float or returns NaN.
Number.parseInt(string) or Number.parseInt(string, radix(optional) ) : converts a string into integer or returns NaN. Radix is nothing but base, like 10(default),2,16,8 etc 
anything.toFixed() : used to fix decimal places of a value and returns it in string format.
anything.toString() : used to convert the number into string.
anything.toPrecision() : it is used to fix the number of digits in a given number and returns a string. Ex : 1234.56 toPrecision(5) to "1234.5", but for 0.00123 toPrecision(2) = "0.0012"(starting zeros ignored).	
anything.toLocaleString() : coverts an number into local number naming culture.
                          example: let num=new Number(100000) num.toLocaleString(en-IN) is represented as 1,00,000 in indian standards, 100,000 in US standards use en-US.
anything.valueOf(),anything.toExponential()    

Note : whenever we use dot(.) on primitive's then a object is created which is wrapper around the primitive.so that we can use all useful
	   properties and methods on the primitive.

Math :
  
math properties : Math.PI, Math.E etc
math methods : Math.sqrt() ,min(),max(),pow(),round(),log(),exp()
ceil() // max roundoff 4.4 = 5
floor() // min roundoff 4.9 = 4
abs() // it only returns value ex : abs(-5) = 5
random() // generates values between 0 and 1(exclusive), like 0.1 or 0.231 
trunc() : returns integer part of a float.
etc

Date and Time :
	the time is calculated from 1 jan,1970 in milliseconds.
 	ex : let time = Date.now() // 1737901708692 this value is in millliseconds from 1 jan 1970 // dont use new keyword here for now() method
  	Syntax : let date = new Date()
   		date.getTime() // 1737901708692 this value is in millliseconds from 1 jan 1970
  	Date have getXYZ() and setXYZ() methods and toString(),toLocaleString() etc.

Arrays :

collection of elements of same or mixed datatypes.
It's index starts from 0 and goes till length-1 for last element.
syntax : use square brackets [] or use Array().
Array() can be called with or without new keyword.
Array() // [] empty array
Array(element1)
Array(element1, element2)
Array(element1, element2,......elementN)
Array(arrayLength)
Note : if Array() has only one input and if that is a number, then it is considered as array length or else it is considered as array element.

example : 
let a = Array(1,2,3) // [1,2,3]
let b = Array(3) // array of length 3, not array element
let c = Array("abhi") // array containing single element ["abhi"]
let  arr = [1,2,3,4,5]
let array = new Array(1,2,3,4,5) // [1,2,3,4,5]

arr[0] // accessing array element using index number, output : 1

Array properties :
arr.length // 5

Array Methods : 

Array.isArray() // determines whether the passed value is Array or not.( true or false)
Array.of() // creates a new Array by input values.
Note : The difference between Array.of() and the Array() is in handling single values, Array.of(7) creates an array with a single element 7, whereas Array(7) creates an empty array with a length of 7.
Array.from() : creates a new array from passed value, it can be string or object or anything.
arr.at(index) // returns the value at particular index.
arr.push(6) // adds element at last
arr.pop() // removes last element and returns removed element.
arr.unshift(7) // adds element at first 
arr.shift() // removes first element and returns removed element.
arr.includes() // searches the element and returns true if present or else returns false.
arr.indexOf() // searches the element and returns it's first occurence index or else returns -1.
arr1.concat(arr2) // adds two arrays and returns a new array, original array does not change.
arr.every( callback function ) : returns true, if every element satisfies the function condition or else returns false.
arr.join() // returns a new string by adding all the elements of the array, separated by commas or a specified separator string. If the array has only one item, then that item will be returned without using the 		          separator and if array.length is 0, then empty string is returned.
arr.slice(start,end-1) // returns a new array by extracting a portion of the original array.
arr.splice(start, deleteCount, item1...) // inserts elements at start(index), if deletecount is 0, then it does not delete the element, else it deletes deleteCount number of elements.
arr.toString() // converts all array elements into string, original array does not change.
arr.sort() or sort(compareFn) : sorts the original array in ascending order.
								it converts all the elements into string and then it compares their UTF-16 codes.
								but to avoid this use callback function with a and b variables.
								a represents first element and b represents second element.
								if a-b > 0, then a comes after b
								if a-b < 0, then b comes after a
								a-b == 0, both are same.
arr.some(callback) : returns true if any one element satisfies the function condition else false.
arr.reverse() // reverse's the original array.
arr.flat(depth)	: // it returns a new aray by flattening the original array, by default the depth is 1, depth can be 1,2.....Infinity.
arr.flatMap(callbackFn) : internally it runs map() first, then flat() next.
arr.find(callbackFn) : returns the first element in the provided array that satisfies the provided testing function. If no values satisfy the testing function, undefined is returned.
arr.findIndex(callbackFn) : returns the index of first element in the provided array that satisfies the provided testing function. If no values satisfy the testing function, -1 is returned.
arr.findLast(callbackFn) : returns the first element in reverse order in the provided array that satisfies the provided testing function. If no values satisfy the testing function, undefined is returned.
arr.findLastIndex(callbackFn) : returns the index of first element in reverse order in the provided array that satisfies the provided testing function. If no values satisfy the testing function, -1 is returned.
...etc
// let a=[1,2,3] 
let b=[4,5] 
let c=[a,b] // merging both arrays o/p  : [ [1,2,3] , [4,5]  ] , but if we want o/p as [1,2,3,4,5] use spread operator
let newArr = [...a,...b] // it merges both arrays '...' is spread operater

	   
Object : 

symbol for object is {}
It stores key : value pairs
An object is a collection of properties and methods.
Example : let a = {} // empty object 
we can also create an object by using object(). It can be called with or without using new keyword.
Example : 
let obj1 = new Object() or new Object(value)
let obj2 = Object() or Object(value)
Whatever the value is passed inside the Object(), it creates object of that type.
Note : If the value is null or undefined, it creates and returns an empty object.

let obj = { age : 10, "name" : 20, 0 : 30 }

accessing key from object 
obj.age // 10 
or
obj["age" or 'age'] // 10

adding new key from outside
obj.surname = "biradar"

changing values of the keys
obj.age  = 22

Inside an object, every function must be assigned to a key (property name).

In JavaScript, object keys can only be of two main types internally :
String
Symbol
However, when you use other types, JavaScript automatically converts them to strings.
values can be anything like variables , strings , numbers etc
always use trailing comma for last key value pair. its good practice.

let obj = {
  name: "John",
  age: 25
};
console.log(obj.name); // John

Internally:
"name" → string
"age"  → string

Even numeric keys become strings.

let obj = {
  1: "one",
  2: "two"
};
console.log(obj["1"]); // one

Here:
1 → "1"
2 → "2"

If an object contains only integer's as  keys ( by the way they automatically get converted into string internally).
Now when we print the keys they will be printed in sorted order, it's java script behaviour.

in operator :

ex : let myObject = inserting( "abhishek", 24);
     console.log( name in myObject ); // true 


Object methods :

Object.assign() : It copies all properties from one or more objects to the target object. If only one value is passed, then it will convert it into object.
   				  syntax : Object.assign(target, source1, source2,.....sourceN)   
Object.create() : creates a new object, using an existing object.
				  Example : const newObj = Object.create(oldObj)
Object.entries(obj) : returns an array of arrays, where each array has key-value pair.
Object.freeze(obj) : It freezes an object. so that new properties cannot be added or existing properties cannot be removed and the object's properties and prototype                      cannot be re-assigned. 
				     syntax : Object.freeze(obj)
Object.fromEntries() : transforms a list of key-value pairs into an object. It performs the reverse of Object.entries().
Object.keys(obj) : returns an array of stringed key names.
Object.values(obj) : returns an array of property values.	  
Object.hasOwn() : returns true, if the mentioned property is its own property. If the property is inherited, or does not exist returns false.
	  			  syntax : Object.hasOwn(obj, property)
Object.isFrozen() : returns true, if an object is frozen, else returns false..
hasOwnProperty() : returns true, if the mentioned property is its own property. If the property is inherited, or does not exist returns false.
	  			   syntax : objectName.hasOwn(property)
Object.seal(obj) : It's same as freeze, but it allows us to reassign the values of properties of an object.
Object.defineProperty() : This method defines a new property directly on an object, or modifies an existing property on an object, and returns the object.
						  syntax : Object.defineProperty(obj, prop, descriptor)
						  descriptor are of two types and the descriptor can be only any one of them, They are : 
						  1. data descriptor : value,
						                       writable(can we change the value or not),
											   enumerable(can we acces the property in loop or not),
											   configurable(can we delete the property or not)
						  					   Example : let obj={a:10}
											   			 Object.defineProperty(obj, "b", { value: 20,writable: true,enumerable: true,configurable: true,});
														 console.log(obj.b) // 20
						  2. accessor descriptor : get() and set() methods.
Object.getOwnPropertyDescriptor(obj,"property") : returns an object, describing the configuration of a specific property on a given object . The object returned is 													mutable but mutating it has no effect on the original property's configuration.
...etc
delete keyword is used to delete a specific property in an object.
Example : let obj={a:10}
		  delete obj.a
let a={1:2} 
let b={2:3} 
let c={a,b} // merging both objects o/p  : { {1:2} , {2:3}  } , but if we want o/p as {1:2,2:3} use spread operator
let newobj = {...a,...b}

Functions : A set of statements that performs a particular task.

syntax :

function functionName( arguments  ){

}
functionName(parameters)

Example : 
     
function print( ){
	console.log("abhishek")
}
print() // this function prints only name, it doesn't return any value

let result = print() // here also the function prints only name, it doesn't return any value. If we print result ,its value will be undefined
     
function print( ){
	return "abhishek"
}
let result = print() // here the function  return a value and it's stored in a variable. If we print result ,its value will be abhishek

Example :
function print(a,b){
    console.log(`${a} ${b}`);
}
print(10);
output : 10 undefined

function print(a,b=20){
    console.log(`${a} ${b}`);
}
print(10);
output : 10 20

Parameters are the variables listed in the function definition.
Arguments are the actual values passed to the function when calling it.

function add(a, b) {   // a and b → parameters
  return a + b;
}

add(5, 10);            // 5 and 10 → arguments

// if we want to send multiple arguments at once. we use rest operator.
example : function print( ...num ){
	     	return num
     	  }
          console.log( print(1,2,3)) // it returns an array [1,2,3], here num becomes is an array
		  
arguments object :

example : function print(){
	     	return arguments;
     	  }
          console.log(print(1,2,3)) // [Arguments] { '0': 1, '1': 2, '2': 3 }
    
Anonymus Function : A function without function name. 
Example : let ans = function (){
		    console.log("hello")
          }
console.log(ans) 
// output : 
function (){
	console.log("hello")
}

console.log(ans())  // hello  

Hoisting : calling the function before its creation.
Example :
print()
function print( ){
	console.log("abhishek")
} 
o/p : abhishek

Note : But hoisting is not possible with anonymous function, it will generate an error.
print()
let print = function ( ){
				console.log("abhishek")
			}
 o/p : Error

 Arrow Function : () => {}
 
 example : let ans = (a,b) =>{ return a+b } // explicit return
 console.log(ans(2,3)) // 5
 console.log(ans) // (a,b) =>{ return a+b }

 let ans = (a,b) => a+b  // implicit return , no need to write return if there is only one line of code
 						or
let ans = (a,b) => (a+b)  // implicit return , no need to write return if the code is in ()

Note : But hoisting is not possible with arrow function, it will generate an error.
	   Arrow function does not arguments object.
	   Arrow functions does not have their own this, they inherit this from the outer scope or surroundings.


Method shorthand :

example : 
a() {
  console.log('hi');
}
a() // error

But, it is allowed inside an object or class.
example1 :
const obj = {
  			  a() {
    			console.log('hi');
  			  }
		    };
obj.a(); // hi

example2 :
class Test {
  a() {
    console.log('hi');
  }
}
const t = new Test();
t.a(); // hi

IIFE : imediately invoked function expression ()()
       it is used to get rid of global pollutants.
       (normal function or anonymus function or arrow function)(parameters);
       ex : let a = ( function (name){ return name })('abhishek');
       		console.log(a) // abhishek

Closures : A closure is created when a function “remembers” the variables from its outer scope, even after that outer function has finished executing.

example :
function outer() {
  let count = 0;

  function inner() {
    count++;
    console.log(count);
  }

  return inner;
}

const counter = outer();

counter(); // 1
counter(); // 2
counter(); // 3

Higher order function :

A higher order function is a function that takes another function as an argument or returns another function.
example : above closure example or map(),filter(),reduce(),forEach() etc, these functions take callback function as an argument.

this keyword : this refers to current object and it is used inside the object.
 		if we print only this, then it refers to an empty object = { } in node environment.
   		But in browser, this refers to global object that is Window{}
		
Operators :

 1. Arithmetic operators : +, -, *, /, %, **(exponentiation), ++(increment){ pre ++, post ++ }, --(decrement){ pre --, post -- }
 2. Number + string : It will convert number into string, other operators will convert the string to number.
 3. Comparison operators : >, >=, <, <=, ==(equal only checks values), !=(not equal only checks values), ===(strict equal checks values and datatypes), !==(strict not equal checks values and datatypes)
 4. assignment operators : =, +=, -=, *=, /=, %=, **= etc Example: let a += 10 ( a=a+10)
 5. Logical operators : Logical and (&&) : returns true if all the conditions are true, else it returns false.
			Logical or (||) : returns true if any one of the condition is true, else it returns false.
    			Logical not (!) : it converts true to false and false to true.
    			null coalescing operator ( ?? ) : value1 ?? value2. if value1 is null or undefined it will return value2 or else it will return value1
 6. bitwise operators : |, &, ^, ~, >>, <<, >>>
 7. Ternary operator : condition ? true part : false part. If condition is true returns true part and if condition is false then it returns false part.
    		       Example : let age = 18
    				 let ans = (age >= 18)? 'can vote' : 'cannot vote'
 falsy values : false, 0, null, undefined, NaN, "" are considered as falsy values.
 truthy values : All other values including all objects evaluate to true when passed to a conditional statement.
// in, instanceof, typeof,new, super etc are also called as operators
 conditional statements :
  1. if( condition ){
     
	}
  2. if( condition ){
     
     }else{
     
     }
 3. if( condition ){
     
     }else if(){
     
     }else{
    
    }
 4.switch (expression) {
	case label1: statements1;
    			break;
  	case label2: statements2;
                break;
 	 so on
  	default: statementsDefault;
}

Loops : easy way to do something repeatedly. 
1. for loop :
   syntax : for ( initialization; condition; increment or decrement ){
   
            }
2. while loop :
   syntax : while( condition ){
   
            }
3. do while loop :
   syntax : do{
   
            }while( condition )
break statement : it is used to come out of the loops and switch statement.
example : for(let i = 0;i<5;i++){
	   console.log(" hi ")
    	   break
	   console.log(" hello ")
}
o/p : hi 
continue statement : it is used to ignore the current iteration and move to the next iteration.
example : for(let i = 0;i<5;i++){
	   
    	   if( i == 3){
		console.log("you skipped printing 3 by using continue")
  		continue
	   }   
    	   console.log(i)
}
o/p : 0
      1
      2
      you skipped printing 3 by using continue
      4

4.for of loop : It is used to get values.
                syntax : for(iterator of iterable){
                         }
	            example : let arr = [1,2,3,4,5]
 		                  for(let i of arr){
     			               console.log(i)
		                  }
    		              o/p : 1 2 3 4 5
Note : itrerables can be array,string,map but not object, because object is not iterable. so use Object.keys(), Object.values(), or Object.entries() with objects for looping.
5.for in loop : It is used to get keys or index's. 
                syntax : for(iterator in iterable){
                         }
	            example : let arr = [1,2,3,4,5]
 		                  for(let i in arr){
     			              console.log(i)
		                  }
    		             o/p : 0 1 2 3 4 // here indexs are considered as keys
      		             let obj = { name : 'abhi',age : 22 }
		                 for(let i in obj){
  			                   console.log(i) // name age are keys
		                 }
  		                 for(let i in obj){
  			                   console.log(obj[i]) // 'abhi' 22
		                 }
Use for...of for Arrays, Strings, Maps, Sets
Use for...in for Objects
Avoid for...in for arrays (can cause bugs)

callback function : A function which is passed as an argument to another function is called as callback function.

6.forEach( callback function) or forEach( callback function,this(optional)) : 
	foreach is generic method used to perform operations
	callback function - it can be arrow function or  anonymus function.
        The arguments of callback function are element, index,array.
        The name of the arguments can be anything, but their order cannot be changed.
        Return value of callback function is ignored.
        forEach only returns undefined.
		we cannot use break,continue in forEach.
		forEach accepts only synchronous function, it does not wait for promises.
7.array.filter(callback function) or filter(callback function,this(optional):
     callback function - it can be arrow function or  anonymus function.
     The arguments of callback function are element, index,array.
     The name of the arguments can be anything, but their order cannot be changed.
     Filter function returns an array.
     If callback function returns truthy value, then only it will add the current element in the result array.
8.array.map(callback function) or map(callback function,this(optional):
     map is generic method used to perform operations
     callback function - it can be arrow function or  anonymus function.
     The arguments of callback function are element, index,array.
     The name of the arguments can be anything, but their order cannot be changed.
     map function returns an array.
     the value returned by the callback function is added in the result array.
9.array.reduce( callback function ) or reduce( callback function, initialvalue ) :
	reduce is generic method used to perform operations
	callback function - it can be arrow function or  anonymus function.
 	The arguments of callback function are accumalator(result),element, index,array.
  	The name of the arguments can be anything, but their order cannot be changed.
   	reduce only returns an single value that is accumalator value.
    	the return value of callback function is stored in accumalator at every stage till the end of the array.
    	if we specify the initialvalue and it can be anything, then the accumalator value at first will be initial value.
     	if we don't specify the initialvalue, then the accumalator value at first will be 0th index value and element will be pointing to 1st index value .
example :

const numbers = [1, 2, 3, 4];
const sum = numbers.reduce((accumulator, currentValue) => {
  return accumulator + currentValue;
}, 0);
console.log(sum); // 10

What actually happens step-by-step :

Iteration	accumulator	currentValue	returned value	next accumulator
1	           0	             1	           1	              1
2	           1	             2	           3	              3
3	           3	             3	           6	              6
4	           6	             4	          10	             10

The value you return becomes the accumulator for the next iteration.
So:
accumulator + currentValue → just computes
return accumulator + currentValue → stores it as the next accumulator

overview of an class : class have{ 
				variables/properties/attrributes
    				functions/methods/behaviour
                       }

Destructuring in JavaScript :

Destructuring is a convenient way to extract values from arrays or objects and assign them to variables in a cleaner way.

1️. Array Destructuring

Basic Example

const numbers = [10, 20, 30];
const [a, b, c] = numbers;
console.log(a); // 10
console.log(b); // 20
console.log(c); // 30

Skipping Values

const [first, , third] = numbers;
console.log(third); // 30

Default Values

const [x = 5, y = 10] = [1];
console.log(x); // 1
console.log(y); // 10

Rest Operator

const [head, ...tail] = [1, 2, 3, 4];
console.log(head); // 1
console.log(tail); // [2, 3, 4]

2️. Object Destructuring : In object destructuring, the variable name must match the property name in the object.

Basic Example
const user = {
  name: "Alice",
  age: 25
};

const { name, age } = user;
console.log(name); // Alice
console.log(age);  // 25

Renaming Variables

const { name: userName } = user;
console.log(userName); // Alice

Default Values

const { country = "USA" } = user;
console.log(country); // USA

Nested Destructuring

const person = {
  id: 1,
  address: {
    city: "New York",
    zip: 10001
  }
};

const { address: { city } } = person;
console.log(city); // New York

3️. Destructuring in Function Parameters

function greet({ name, age }) {
  console.log(`Hello ${name}, age ${age}`);
}
greet({ name: "Bob", age: 30 });

With default values:

function greet({ name = "Guest" } = {}) {
  console.log(`Hello ${name}`);
}

4️. Swapping Variables (Common Trick)

let a = 1;
let b = 2;
[a, b] = [b, a];
console.log(a); // 2
console.log(b); // 1

important :
why do we assign {} in function or object ?
If nothing is passed, just use an empty object instead.
example : 

function greet({ name }) {
  console.log(name);
}
greet(); // ERROR

Why?
Because when you call : greet()
JavaScript tries to do : const { name } = undefined;
And you cannot destructure undefined or null.

Why We Assign = {}

function greet({ name } = {}) {
  console.log(name);
}

Now when you call : greet()

It becomes:
const { name } = {};
And destructuring {} is safe.
Result : undefined

Nested Objects :

const user = {};
const { profile: { name } } = user; // ERROR
Because : user.profile === undefined
So JS tries to do : const { name } = undefined;

correct way :

const user = {};
const { profile: { name } = {} } = user;
console.log(name); // undefined
Now if profile doesn't exist, it defaults to {}.


Strict Mode in JavaScript :

Strict Mode is a way to a safer, stricter version of JavaScript.
It helps you catch common mistakes and prevents unsafe behavior.
You enable it by adding : "use strict";

Strict mode changes:

Feature	               Normal Mode	   Strict Mode
Undeclared variable	  Becomes global	Error
this in function	  Global object	    undefined
Primitive this	          Boxed	        Not boxed
arguments linking	     Linked	        Not linked
Silent errors	         Ignored	        Throw error

Important:
Classes are always in strict mode. Even if you don’t write "use strict".
You cannot delete variables in strict mode.
Duplicate parameter names not allowed in strict mode.
Arrow function inherits this from surrounding function.
Duplicate Object Keys is allowed now (last one wins). Error in old versions.


Hoisting :

Declaration: creates the variable name in memory (but doesn’t necessarily give it a value yet).
Initialization/assignment: actually gives the variable a value.
Hoisting in JavaScript is the behavior where declarations (not initializations) are conceptually moved to the top of their scope before code execution. This can make variables and functions accessible earlier than they appear in the code.

Key Points About Hoisting :

Function Declarations: Fully hoisted. You can call a function before it’s defined.
var Declarations: Hoisted but initialized with undefined. You can reference them before declaration, but they won’t hold a value yet.
let and const Declarations: Hoisted but remain in the Temporal Dead Zone (TDZ) until initialized. Accessing them before declaration throws a Reference Error.

Initializations are NOT hoisted, only the declaration part is.
var gives you undefined before assignment.
let and const are hoisted but inaccessible until declared (TDZ).
Functions declared with function are fully hoisted.


new keyword :

The new keyword in JavaScript is used to create an instance (object) from a constructor function or class.
It tells JavaScript : “Create a new object based on this constructor.”

JavaScript does 4 things behind the scenes :
1️. Creates a new empty object by using new keyword
2️. links the empty object's prototype to constructor function prototype
3️. Sets this to the new object
4️. Returns the new object automatically

what is prototype ?
prototype is an Object.

constructor :

A special function/method that runs automatically when a new object is created, used to initialize object properties.
It sets up the initial properties and values when a new object is created.
Before ES6, JavaScript only had constructor functions, not the class syntax.
Even modern classes are still syntactic sugar over constructor functions.

There are two main ways constructors are used in JavaScript:

1️. Constructor Function (Traditional Way)
function Person(name, age) {
  this.name = name;
  this.age = age;
}

const user1 = new Person("Alice", 25);
console.log(user1.name); // Alice

2️. Constructor in a Class (Modern Way - ES6)
With ES6 classes, the constructor is a special method named constructor.

class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
}

const user1 = new Person("Alice", 25);
console.log(user1.age); // 25

Important rules:
A class can have only one constructor.
The constructor runs automatically when you use new.
If you don’t define one, JavaScript provides a default empty constructor.


What Happens Without new ?

function Person(name) {
  this.name = name;
}

const user = Person("Alice"); // missing new

Without new:
here we are ony calling the Person function and it's not returning anything and user is not an object.
this may refer to the global object (or undefined in strict mode)
It can cause bugs


Factory Function (No new) :

function createPerson(name) {
  return {
    name, // instead of writing : name : name
    sayHello() {
      return "Hello " + name;
    }
  };
}

const user2 = createPerson("Bob");
No new and No this in above code.

Note : usually don’t use new for String, Number, and Boolean, because new creates an object, not a primitive.


is it mandatory to use prototype in constructor to write methods ?
No, it is not mandatory to use prototype to write methods in a constructor.
But using prototype is usually better for memory efficiency.

Option 1: Method Inside Constructor (No prototype)
function Person(name) {
  this.name = name;

  this.sayHello = function () {
    return "Hello " + this.name;
  };
}

const user1 = new Person("Alice");
const user2 = new Person("Bob");

What happens?
Each time you create a new object, a new copy of sayHello is created.
user1.sayHello !== user2.sayHello
That means more memory usage.

Option 2: Method on Prototype (Recommended)
function Person(name) {
  this.name = name;
}

Person.prototype.sayHello = function () {
  return "Hello " + this.name;
};

const user1 = new Person("Alice");
const user2 = new Person("Bob");

What happens?
Only one copy of sayHello exists.
All objects share it.
user1.sayHello === user2.sayHello
More memory efficient 


Prototypal Inheritance in JavaScript :

Prototypal inheritance means that objects can inherit properties and methods from other objects through the prototype chain.
In JavaScript, inheritance is based on objects inheriting from objects, not classes (even though we use class syntax).

Every object in JavaScript has an internal link to another object called its prototype.

When you try to access a property:

JavaScript checks the object itself.
If not found, it checks its prototype.
If still not found, it checks the prototype’s prototype.
This continues until null.
This is called the prototype chain.

example : check 14th file of cohort or explore on internet.


What is a Polyfill in JavaScript?
A polyfill is writing our code for newer JavaScript features in older browsers that don’t support them.


garbage collection : it's done automatically in java scrpit. It cleans unreachable things.

ex : let obj={ name : 'abhishek",
		age : 23,
	}

here this part { name : 'abhishek",
		age : 23,
	     } 
is reachable by using obj variable.

obj=null;
here this part { name : 'abhishek",
		age : 23,
	     } 
is not reachable by using obj variable.so that is cleaned by garbage collector.


optional chaining : it's new and cleaner way to access nested object property value.
		    if the property is present then it returns it's value or it returns undefined.
		    it is represented by ( ?. )
ex : let obj={ name : 'abhishek",
		age : 23,
		address : { pincode : 500018,
			    city : HYD,
			    locality : Moti Nagar,
	     }
console.log(obj.address?.city); // HYD is printed


Map :

map object is similar to normal object, but the difference is that here the key can be of any type, whereas in object the key can be symbol or string.

map allows only unique key's, if a key is repeated, then the latest key is considered.
insertion order of keys is preserved.
 
1. creating a map object

ex : let map = new Map();

2. set(key,value) : it set's key - value pair in the map object.

ex : map.set('name',"abhishek");

3. get(key) : it gets the value of a key from the map object.

ex : map.get('name'); // "abhishek"

4. size : this gives the size of number of key-value pairs in map object.

ex : map.size; // 1

5. clear() : it clears all the key - value pairs from the map object.

ex : map.clear();
     map.size; // 0

6. has() : this method is used for checking whether an key is present in map or not.

ex : map.has('name'); // true

7. delete() : this method is used for deleting an particular key.

ex : map.delete('name');

keys() gives an map iterator, values() gives an map iterator etc

iterator is an object
iterator has all the elements
we can only access one element at a time.
iterator also has an next() method, which returns an object.
the returned object has a value property which has the current element and it also has done property which has true or false value.

ex : let it = map.keys();
console.log(it.next().value); // "name"

Iterability : object that has Symbol.iterator method and can be looped via iteration protocols (for...of, spread, etc.), but not all loops count.
In JavaScript, objects are broadly divided into iterables and non-iterables.

An object is iterable if it implements the Symbol.iterator method. This method must return an iterator - an object with a next() method that tells JavaScript how to get the next value.

Common iterables

Arrays → [1, 2, 3]
Strings → "hello"
Maps → new Map()
Sets → new Set() ...etc

Non-Iterables

These do NOT have Symbol.iterator method by default. If we want to make them iterable we should implement Symbol.iterator method in them.

Common non-iterables

Plain objects
null
undefined
weakest
weakmap ...etc


set :

set object stores only unique values in it.

1. creating a set object

ex : let set = new Set();

2.add() : inserts the value in the set.
3.clear() : clears all the elements from the set.
4.delete() : it delete's specified value from the set.
5.difference() : it returns an set with difference values.
                 ex : set1.difference(set2); // unique values in set1 are returned.
6.has() : returns a boolean value, if the specified value exists in this Set or not.
7.intersection() : it returns a set of similar values between two sets.
                   ex : set1.intersection(set2);
8.isDisjointFrom() : takes a set and returns a Boolean value if this set has no elements in common with the given set.
                    ex : set1.isDisjointFrom(set2);
9.isSubsetOf() : takes a set and returns a boolean value if all elements of this set are in the given set.
		ex : set1.isSubsetOf(set2);
10.keys() and values() : both the methods are same and returns an iterator for values of the set.
11. union() : it returns an set of unique values present in both sets.
12. size : this property returns the size of the set.
...etc


WeakMap :

A WeakMap is like a Map.
Keys must be objects (no primitives)
Keys are weakly referenced -> can be garbage collected

Example : 

const wMap = new WeakMap();

let obj = { name: "John" };

wMap.set(obj, "some data");

console.log(wMap.get(obj)); // "some data"

Key Feature : Weak Reference

let obj = { name: "John" };

const wm = new WeakMap();
wm.set(obj, "data");

// remove reference
obj = null;

Now the original object has no references
It becomes eligible for garbage collection
The entry in WeakMap is automatically removed (eventually)
whereas the entry in Map is not removed

Allowed Keys

const wm = new WeakMap();

wm.set({}, "ok");      // allowed
wm.set([], "ok");      //  allowed
wm.set(() => {}, "ok");//  allowed

wm.set(1, "no");       //  Error
wm.set("key", "no");   //  Error

-> Only objects are valid keys

Only Methods of WeakMap 

wm.set(key, value);    // add/update
wm.get(key);           // get value
wm.has(key);           // check existence
wm.delete(key);        // remove entry

wm.size        //  not available
wm.keys()      // not available
wm.values()    // not available
wm.entries()   // not available
for...of       //  not iterable


WeakMap vs Map

Feature	            Map 	WeakMap 

Key types	        Any	       Only objects
Garbage collection  No	       Yes (automatic)
Iterable	        Yes	       No
Size property	    Yes	       No


WeakSet :

A WeakSet is a collection of unique objects, where:

Only objects are allowed (no primitives)
Objects are weakly referenced (can be garbage collected)
Values are unique (like Set)

Example

const ws = new WeakSet();

let obj1 = { name: "A" };
let obj2 = { name: "B" };

ws.add(obj1);
ws.add(obj2);

console.log(ws.has(obj1)); // true

Weak Reference Behavior

let obj = { data: 123 };

const ws = new WeakSet();
ws.add(obj);

// remove reference
obj = null;

 Now the object has no references
 It becomes eligible for garbage collection
 It will be automatically removed from the WeakSet
 whereas the entry in Set is not removed

Allowed Values

const ws = new WeakSet();

ws.add({});       //  allowed
ws.add([]);       //  allowed

ws.add(10);       //  Error
ws.add("hello");  //  Error

Only objects can be stored

Methods of WeakSet

ws.add(obj);      // add object
ws.has(obj);      // check if exists
ws.delete(obj);   // remove object
 
WeakSet does NOT support :

ws.size        // not available
ws.keys()      // not available
ws.values()    // not available
ws.entries()   // not available
for...of       // not iterable

Because items can disappear anytime due to garbage collection

WeakSet vs Set

Feature  	        Set  WeakSet 

Value types	        Any  Only objects
Duplicates	        No   No
Garbage collection  No	Yes
Iterable	        Yes	 No
Size property	    Yes	 No
