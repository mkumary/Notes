
```
if (something) {
	function foo() {
		console.log( "1" );
	}
}
else {
	function foo() {
		console.log( "2" );
	}
}
var something = true;
foo();    //2
```


this will print true no matter what is the value of something because of hoisting.

but even while hoisting engine remains smart enough to surprise for below code.

```

if (true) {
	function foo() {
		console.log( "1" );
	}
}
else {
	function foo() {
		console.log( "2" );
	}
}

foo();    //1

```





