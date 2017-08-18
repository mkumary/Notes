``` 



function DataStructure(){
        var map = {};
        var arr = [];
        // function to swap two numbers in a array
        var swap = function(arr, start, end){
                var p = arr[start];
                arr[start] = arr[end];
                arr[end] = p ;
                return arr;
        }

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
                         if(last!== number)   {    // no need to swap or add again incase of last index of array.  
                                swap(arr, hashIndex,  size-1);
                                // Update hash table for new index of last element
                                map[last] = hashIndex;
                        }
		           // Remove last element (This is O(1))
                           arr.pop();

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


// test above code.
var ds = DataStructure();
ds.add(3);
ds.add(45);
ds.add(32);
ds.add(7);
ds.add(34);
ds.remove(45);
ds.search(7);
ds.getRandom();
```

