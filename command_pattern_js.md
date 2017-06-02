```
var calculator = {

add : function(a,b){
  return a+b;
},
mul : function(a,b){
  return a*b;
}

}

```

Now I want to pass commands that it can use to run a perticular funciton.

for eg: 

```
calculator.run('add')
```


now lets define this function:

```

calculator.run = function ( name ) {
    return calculator[name] && calculator[name].apply( calculator, [].slice.call(arguments, 1) );
};

```

testing

```
calculator.run('add', 4, 3)   // 7
calculator.run('mul', 4, 3)   // 12

```
