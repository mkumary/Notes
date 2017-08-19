```

Array.prototype.shuffle = function(){
  var i = this.length, j, temp;
  while(--i > 0){
    var j =  Math.round(Math.random(this.length))
    temp = this[i];
    this[i] = this[j];
    this[j] = temp;
  }
return this;
}



['A', 'B', 'C', 'D'].shuffle()  //["D", "C", "B", "A"]
['A', 'B', 'C', 'D'].shuffle()  //["D", "C", "B", "A"]
['A', 'B', 'C', 'D'].shuffle()  //["C", "A", "D", "B"]
['A', 'B', 'C', 'D'].shuffle()  //["B", "C", "D", "A"]
['A', 'B', 'C', 'D'].shuffle()  //["C", "A", "D", "B"]

```
