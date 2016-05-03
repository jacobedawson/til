//cloning an array w/o reference to original

var x = [];
var y = x; //y = x creates makes y a direct reference to x
var z = x.slice(0); //x.slice(0) returns a new array

console.log(x); //[]
console.log(y); //[]
console.log(z); //[]

x.push('value'); //add a value to x

console.log(x); //['value']
console.log(y); //['value'] y is still just a reference to x
console.log(z); //[] z is an independent object and does not push or receive changes from x