# javascript
Node js allows developers to write JavaScript code that runs directly in a computer like in vs codes terminal itself instead of in a browser. There are also other js environment other than node.js like deno.js etc
If we don't install node.js then we cant run js file in vs code's terminal.
node -v command is used for checking the version of node.js or to check whether node is installed or not.
node filename.js to execute js file.

console.log() - is used for printing.
console.table([a,b,c,d] - is used for printing multiple variable's value at once.
// is used for single line comment.
/* */ is used for multi line comment's.
variables in js :

constant : constant variables value cannot be changed after assigning a value to it.
example : const myName = "abhishek" 
          myName="abhi" // error
let : mostly used variable  is let.variables value can be changed after assigning a value to it.
example : let myName = "abhishek"
           myName="abhi" // no error
var :  var is not used commonly because of it's issue in block scope and functional scope. var was widely used in older version's of javascript.
nothing : No keyword is used for defining a variable here.
Example :  myName="abhi" // no error

Data Types:
  
7  Primitive Datatypes:
	
Null : 	It's value  is nothing.
Example : let a = null 

Undefined : It is nothing but not assigning a value to a variable.
Example : let a 
	  console.log(a) // undefined
	
Boolean	 : It has two values true and false.
Example : let ans = true or false
	
Number : Both integers and float values come under Number datatype.
Example : let a = 10
	  let b = 11.1
	
BigInt : It is used to very large integer values.
Example : let a = 99999n
	
String : It is collection characters enclosed in single or double quotes.
Example : let name = "Abhishek"
	           	
Symbol	: It is used for making a value or anything as unique.(not a correct definition)
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

Typeof	        typeof return value	

Null	           "object"	
Undefined	 "undefined"	
Boolean	          "boolean"	
Number	           "number"	
BigInt	           "bigint"	
String	           "string"	
Symbol	           "symbol"

Non Primitive Datatypes : Arrays, objects, functions etc


Backticks : ` `
example : let name = "abhi"
	  let age = 22
	  console.log(` my name is ${name} and I am ${age} years old `) // instead of "my name is" + name + "and I am" +age+ "years old"

String as an object :
 
let name1 = "abhi" // typeof name1 is string
let name = String("abhi") // typeof name is string
let name2 = new String ("abhishek" )  // typeof name2 is object

Few string methods : length,chartAt() concat() indexOf() toUpperCase() toLowerCase() startsWith() endsWith() replace() includes() padStart(finalstringlength,value) padEnd() repeat() replace() replaceAll() slice() split() split returns an array substring() toString() trim() trimStart() trimEnd()
