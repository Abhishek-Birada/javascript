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
	
String : It is collection of characters enclosed in single or double quotes.
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

Non Primitive Datatypes : Arrays, objects, functions etc // Non Primitive Datatypes are passed as reference that means if we change value of one variable the value also gets changed in another variable unlike primitive datatypes . example : let a = 10
				let b = a // b = 10
    				b = 9 // here b value changes but a value doesn't change 
				let a = [1,2,3]
    				let b = a // b = [1,2,3] b and a point to [1,2,3]
				b.push(4) // b array changes and a array also changes because a and b point to same array 


Backticks : ` `
example : let name = "abhi"
	  let age = 22
	  console.log(` my name is ${name} and I am ${age} years old `) // instead of "my name is" + name + "and I am" +age+ "years old"

naming convension : pascal case : first letter of every word should be capital. example : Abhishek or AbhishekBiradar // this convension is used for class names
		    camel case : except first word, first letter of other words should be capital example : abhishek or abhishekBiradar // this convension is used for variables,method names etc
overview of an class : class have{ 
				variables/properties/attrributes
    				functions/methods/behaviour
                       }
// object in js are different from objects in other languages. object in js ex : let obj = { key : value }
String as an object :

new keyword is used create an object 
let name1 = "abhi" // typeof name1 is string
let name = String("abhi") // typeof name is string
let name2 = new String ("abhishek" )  // typeof name2 is object // internally name2 = { }
Few string properties : length
Few string methods : chartAt() concat() indexOf() toUpperCase() toLowerCase() startsWith() endsWith() replace() includes() padStart(finalstringlength,value) padEnd() repeat() replace() replaceAll() slice() split() split returns an array substring() toString() trim() trimStart() trimEnd()

Number as an object :

let num = new Number(10) // typeof num is object not number
number properties : MAX_VALUE or MIN_VALUE etc
number methods : toFixed() used to fix decimal values
		 toString() 
		 toLocaleString() coverts an number into local number naming culture example: let num=new Number(100000) num.toLocaleString(en-IN) is represented as 1,00,000 in indian standards, 100,000 in US 		 standards use en-US.
                 toPrecision() etc

Math :
  math properties : Math.PI etc
  math methods : Math.sqrt() ,min(),max(),pow(),round(),log()
  ceil() // max roundoff 4.4 = 5
  floor() // min roundoff 4.9 = 4
  abs() // it only returns value ex : abs(-5) = 5
  random() // generates values between 0 and 1, like 0.1 or 0.231 etc

Date and Time :
	the time is calculated from 1 jan,1970 in milliseconds.
 	ex : let time = Date.now() // 1737901708692 this value is in millliseconds from 1 jan 1970 // dont use new keyword here for now() method
  	Syntax : let date = new Date()
   		date.getTime() // 1737901708692 this value is in millliseconds from 1 jan 1970
  	Date have getXYZ() and setXYZ() methods and toString(),toLocaleString() etc.

Arrays :

collection of elements of same and mixed datatypes.
syntax : let  arr = [1,2,3,4,5]
	 let array = new Array(1,2,3,4,5)
  	 console.log(arr) // [1,2,3,4,5]
    	 arr[0] // 1
    	 arr.length // 5
    	arr.push(6) // adds element at last
     	arr.pop() // removes last element
      	arr.unshift(7) // adds element at first 
        arr.shift() // removes first element
	arr.includes(1) // true
 	arr.indexOf(1) // 0
       arr.concat(array) // adds two arrays and returns an concatenated array [1,2,3,4,5,1,2,3,4,5]
       arr.join(array) // adds two arrays but returns an string with specified separator without square brackets 1,2,3,4,5,1,2,3,4,5
       arr.slice(0,n-1) // ex : n=3 returns an array [1,2,3]
       arr.splice(0,n) // n=3 returns an array [1,2,3,4] and it also changes the original array that is arr = [5]
       // let a=[1,2,3] 
       	  let b=[4,5] 
	  let c=[a,b] // merging both arrays o/p  : [ [1,2,3] , [4,5]  ] , but if we want o/p as [1,2,3,4,5] use spread operator
       let newArr = [...a,...b] // it merges both arrays '...' is spread operater
       flat,isArray,from,of
Object : symmbol for objects is {}
	 An object is a collection of properties, and a property is an association between a name (or key) and a value. A property's value can be a function, in which case the property is known as a method.
	 It stores key : value pairs 
  	 syntax : let a = {} // o/p : {} this is empty object 
    	         let b = new Object() // o/p : {} this is also an empty object 
  	 Key and values cane be anything like variables , strings , numbers  etc let obj = { age : 10, "name" : 20, 0 : 30 }
    	// accessing key from object 
    	 obj.age // 10 or obj["age" or 'age'] // 10
      // adding new key from outside
      obj.surname = "biradar"
      // changing values of the keys
      obj.age  = 22
      let a={1:2} 
       	  let b={2:3} 
	  let c={a,b} // merging both objects o/p  : { {1:2} , {2:3}  } , but if we want o/p as {1:2,2:3} use spread operator
	 let newobj = {...a,...b}

  Functions :
     function functionName( parameters ){

     }
     functionName(arguments)

     function print( ){
	console.log("abhishek")
     }
     print() // this function prints only name, it doesn't return any value

     function print( ){
	console.log("abhishek")
     }
     let result = print() // here also the function prints only name, it doesn't return any value. If we print result ,its value will be undefined
     function print( ){
	return "abhishek"
     }
     let result = print() // here the function  return a value and it's stored in a variable. If we print result ,its value will be abhishek

     // if we want to send multiple arguments at once. we use rest operator.
     example : function print( ...num ){
	     return num
     }
    console.log( print(1,2,3)) // it returns an array [1,2,3] here num becomes an array

    Scope :
    let and  const variables are block scope. That means variables are only available inside a block not outside the block.
    var variables are global scope. That means variables are available throughout the code
    
