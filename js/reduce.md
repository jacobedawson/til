//You can use the reduce() method to perform some pretty cool tricks on array values in JavaScript: 

Link: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce

1.) Merge a group of arrays into a single array: 

var flattened = [[0, 1], [2, 3], [4, 5]].reduce(function(a, b) {
  return a.concat(b);
}, []);

//flattened = [0,1,2,3,4,5]


2.) Find the sum total of values in an array:

var x = [1, 2, 464, 325, 356].reduce(function (a, b) {
  return a + b;
});

//x = 1148

2A.) Use an Arrow Function to Reduce Verbosity: 

var x = [1,2,464,325,356].reduce((a,b) => a+b);

//x = 1148