//sort numerical array with compare function
var x = [1,65,2,7,4,8,34];

var y = x.sort(function(a,b) {
	console.log(a-b);
	return a - b;
});

//1 - 65 = -64
//negative number, a (1) is assigned a lower index
//[1,65,2...]

//65 - 2 = 63
//positive number, b (2) is assigned a lower index
//[1,2,65...]