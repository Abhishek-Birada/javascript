# javascript
Node js allows developers to write JavaScript code that runs directly in a computer like in vs codes terminal itself instead of in a browser. There are also other js environment other than node.js like deno.js etc
Node js helps in executing the js file and dispalys the output
If we don't install node.js then we cant run js file in vs code's terminal.
node -v command is used for checking the version of node.js or to check whether node is installed or not.
node filename.js to execute js file.

console.log() - is used for printing.
console.table([a,b,c,d] - is used for printing multiple variable's value at once.
// is used for single line comment.
/* */ is used for multi line comment's.
At the end of the line you can use ; or you can ignore using it
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
    
Anonymus Function : A function without function name. 
Example : let ans = function (){
		    console.log("heelo")
}
console.log(ans) // output : function (){
		                 console.log("heelo")
				}
console.log(ans())  // hello  

Hoisting : calling the function before its creation.
 Example :
 print()
 function print( ){
	console.log("abhishek")
 } 
 o/p : abhishek
 But hoisting is not possible with anonymous function, it will generate an error.
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
let ans = (a,b) => (a+b)  // implicit return , no need to write return if there is only one line of code

 this keyword : this refers to current object and it is used inside the object.
 		if we print only this, then it refers to an empty object = { } in node environment.
   		But in browser, this refers to global object that is Window{}

Operators :

 1. Arithmetic operators : +, -, *, /, %, **(exponentiation), ++(increment){ pre ++, post ++ }, --(decrement){ pre --, post -- }
 2. Comparison operators : >, >=, <, <=, ==(equal only checks values), !=(not equal only checks values), ===(strict equal checks values and datatypes), !==(strict not equal checks values and datatypes)
 3. assignment operators : =, +=, -=, *=, /=, %=, **= etc Example: let a += 10 ( a=a+10)
 4. Logical operators : Logical and (&&) : returns true if all the conditions are true, else it returns false.
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
Map object : It stores key value pairs same as object.
	     But the insertion order of keys is remembered by map and object doesnt remember insertion order of keys.
      	     Map only inserts unique keys unlike object.
	     syntax : let map = new Map()
     	     map.set(key,value) is used to insert key and value pairs in map.
             map.get(key) is used to get the value of the key.
	     map.size property is used to get the size of the map.
      	     map.delete(key) removes a particular key from the map.
	     map.clear() removes all the key value pairs from the map.
      	     map.keys() returns an object of  all the keys.
	     map.values() returns an object of all the values.
             map.has(key) returns true or false based on if key is present in the map or not.
4.for of loop : It is used to get values.
	syntax : for(iterator of iterable){
 
	            }
	example : let arr = [1,2,3,4,5]
 		  for(let i of arr){
     			console.log(i)
		  }
    		o/p : 1 2 3 4 5
     itrerables can be array,string,map but not object,because object is not iterable.
5.for in loop : It is used to get keys. 
		keys of array are indexs.
6.forEach( callback function) or forEach( callback function,this(optional)) : 
	foreach is generic method used to perform operations
	callback function - it can be arrow function or  anonymus function.
        The arguments of callback function are element, index,array.
        The name of the arguments can be anything, but their order cannot be changed.
        Return value of callback function is ignored.
        forEach only returns undefined.
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
    	if we specify the initialvalue, then the accumalator value at first will be initial value.
     	if we don't specify the initialvalue, then the accumalator value at first will be 0th index value and element will be pointing to 1st index value .
     
  	
