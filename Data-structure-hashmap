``` function swap(arr, start, end){

var p = arr[start];
arr[start] = arr[end];
arr[end] = p ;
return arr;
}
function test(){
var map = {};
var arr = [];

return {
add : function(number){ 
if(map[number] !== undefined )return;
map[number]= arr.length;
arr.push(number);
},
remove : function(number){
var hashIndex = map[number];
if( hashIndex === undefined )return;

delete map[number];

var size = arr.length;
var last = arr[arr.length-1];
        swap(arr, hashIndex,  size-1);

        // Remove last element (This is O(1))
        arr.pop();

        // Update hash table for new index of last element
        map[last] = hashIndex;



},

search : function(number){
return map[number];
},

getRandom : function(){
 return arr[Math.floor(Math.random()*arr.length)];
},
get : function(){
   return map;
},
getArr : function(){
  return arr;
}

}

}

var p = test();

p.add(3);
p.add(45);
p.add(32);
p.add(7);
p.add(34);
p.remove(45);
```

