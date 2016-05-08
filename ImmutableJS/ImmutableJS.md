IMMUTABLE LIST PT.1

//create a normal JavaScript array 
var x = [
    {a:'ok',b:'yes'},//index 0
    {a:'sure',b:'no'},//index 1
    {a:'what',b:'this'}//index 2
];

//turn the array into an Immutable list containing Immutable maps
var thread = Immutable.fromJS(x);//thread is an Immutable list

//get the value using a specific index and key
thread.getIn([2]).get('b'); // -> 'this'

//trying to get an undefined value will return an error
thread.getIn([4]).get('b'); // -> 'Cannot read property 'get' of undefined'

//check if a key exist in this iterable, returns boolean
thread.getIn([0]).has('a'); // -> true

//check if a value exists in the iterable, returns boolean
thread.getIn([1]).includes('sure'); // -> true


IMMUTABLE LIST PT.2

//directly create an Immutable list of values
var x = Immutable.List.of('Paul','John','Ringo','George');

//retrieve a value at index 0
x.getIn([0])// -> 'Paul'

//set a new value at index 0 *returns a new List
var y = x.set(0,'Yoko');

//check the newly created List
Immutable.List.isList(y);// -> true

//retreive the value in List y at index 0
y.getIn([0])// -> 'Yoko'

//x is unchanged
x.getIn([0])// -> 'Paul'

//delete a value at index 1 *returns a new List
var z = x.delete(1);
x.size// -> 4
z.size// -> 3
x.includes('John');// ->true
z.includes('John');// -> false


MAP

//create an Immutable map
var y = Immutable.Map({
 a : "a",
 b : Immutable.List.of(
  'a',
  'b',
  'c',
  Immutable.Map({
   a : "a"
  })
 )
});

//set a new value in a map at key 'a', setting value to 'brand new value' *returns a new map
var z = y.set('a','brand new value');