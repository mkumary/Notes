Creating a singleton Class in javascript : 

```
function SingletonClass(){

if(SingletonClass.prototype.singleInstance){
return SingletonClass.prototype.singleInstance;
}

SingletonClass.prototype.singleInstance = this;

this.firstMethod = function(){
//add your method
}

}
```
To test if class is actually a sigleton

```
var a = new SingletonClass();
var b = new SingletonClass();

console.log(a===b)  //prints true;

```


once object is created by using above method. 
then even if you call this function it will return the object.

for eg: 

```

var a = new SingletonClass();
var b = SingletonClass();

console.log(a===b)   //prints true;

```

 Another way to create a singleton class


```
function FirstClass(){
FirstClass.prototype.value = 'your_value';

FirstClass.prototype.methodName = function(){
  //define your function
}

return FirstClass.prototype;
}


var a = new FirstClass();
var b = new FirstClass();
var c = FirstClass();

a===b   // prints true;

a===c // prints true
```
