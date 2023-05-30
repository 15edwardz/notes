# JavaScript Fundamentals - Intro

## Variable Declarations

let - defining variable that can be changed  
const - can't be changed, must be defined when intialized  
var - original variable declaration, older

## Data Types

Number - int, float  
String  
Boolean  
Undefined  
Null  
Symbol  
Object  
Big Int

## String and Template Literals

```JavaScript
const firstName = 'Edward';
const templateLiterals = 'template literals';
console.log('Without ' + templateLiterals + 'it gets hard to keep track of whitespace and formmatting as the variables increase,' + firstName);
console.log(`Use backticks instead with ${templateLiterals} like this, ${firstName}`);
```
```console
Without template literalsIt gets hard to keep track of whitespace and formmatting as the variables increase,Edward  
Use backticks instead with template literals like this, Edward  
```

## Truthy and Falsy

Truthy Values: Values that will be converted to true, anything that isn't falsy  
Falsy values: 0, '', undefined, null, NaN -- thse values will be converted to false when attempting to convert to boolean  
<table>
<tr>
<td>

```js
console.log(Boolean(0));
console.log(Boolean(undefined));
console.log(Boolean('Edward'));
console.log(Boolean({}));
console.log(Boolean(''));

const num = 0;
if(!num){
    console.log(Boolean(num));
}
```
</td>
<td>

```console 
false
false
true
true
false



false

```
</td>
</tr>
</table>

## Equality Operators
== checks for value equality, no type coercion (JS auto convert types to match). Loose Equality  
=== strict equality no type coercion

<table>
<tr>
<td>

``` js
const age = 18;
const goal = '18';
if(age == goal) console.log("Loose Equality");
if(age === goal) console.log("This will not work");
else console.log("Strict Equality");
```
</td>
<td>

```console


Loose Equality

Strict Equality
```
</td>
</tr>
<tr>
<td>

```js
const favNum = prompt("Your Favorite Number: ");
console.log(favNum);
console.log(typeof favNum);

if (favNum == 23) console.log("Loose");
if (favNum === 23) console.log("No tight equality, wont work");
if (favNum === '23') console.log("Tight");
```
</td>
<td>

```console
23
string

Loose


Tight
```
</td>
</tr>
</table>

Avoid loose equality as it is prone to bugs. Instead use strict equality.  

```js
const day = 'friday';

switch (day) {
  case 'monday': // day === 'monday'
    console.log('Today is Monday');
    break; // Important
  case 'tuesday':
    console.log('Today is Tuesday');
    break;
  case 'wednesday':
    console.log('Today is Wednesday');
    break;
  case 'thursday':
    console.log('Today is Thursday');
    break;
  case 'friday':
    console.log('Today is Friday');
    break;
  case 'saturday':
  case 'sunday':
    console.log('Enjoy the weekend');
    break;
  default:
    console.log('Not a valid day!');
}
```
```console
Today is Friday
```

## Conditional (ternary) Operator

Follows the format: condition <code>?</code> expression if truthy <code>:</code> expression if falsy

```js
const age = 23

age >= 18 ? console.log("Adult") : console.log("Child");
```
```console 
Adult
```