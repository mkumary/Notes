# Notes


evenodd caps  solution : 

```
var sol = "this is a test case";
sol.split('').map(function(element, index){
return (index%2 === 0 ? element.toUpperCase() : element.toLowerCase());
}).join('');

```



addition of multiple of 3 and 5 ;


function solution(number){
  var n3 = Math.floor(--number/3), n5 = Math.floor(number/5), n15 = Math.floor(number/15);
  return (3 * n3 * (n3 + 1) + 5 * n5 * (n5 + 1) - 15 * n15 * (n15+1)) /2;
}


---------****************************************************************---------------------------------------
function chaining chained([a,b,c,d])(input) :      d(c(b(a(input))))

------------***************************************************************-----------------------------------------


function chained(functions) {
  return function(input){
    return functions.reduce(function(input, fn){ return fn(input) }, input);
  }
}




function chained(functions) {
  return function(input){
    return functions.reduce(function(input, fn){ return fn(input) }, input);
  }
}





change to find how many people likes this;



function likes (names) {
  var templates = [
    'no one likes this',
    '{name} likes this',
    '{name} and {name} like this',
    '{name}, {name} and {name} like this',
    '{name}, {name} and {n} others like this'
  ];
  var idx = Math.min(names.length, 4);
  
  return templates[idx].replace(/{name}|{n}/g, function (val) {
    return val === '{name}' ? names.shift() : names.length;
  });
}



