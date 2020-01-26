# Type Conversions

### Converting Numbers to Strings

```javascript
String(x)         // returns a string from a number variable x
String(123)       // returns a string from a number literal 123
String(100 + 23)  // returns a string from a number from an expression

x.toString()
(123).toString()
(100 + 23).toString()
```

### Converting Booleans to Strings

```javascript
String(false)      // returns "false"
String(true)       // returns "true"
false.toString()   // returns "false"
true.toString()    // returns "true"
```

### Converting Dates to Strings

```javascript
String(Date())  // returns "Thu Jul 17 2014 15:38:19 GMT+0200 (W. Europe Daylight Time)"
Date().toString()  // returns "Thu Jul 17 2014 15:38:19 GMT+0200 (W. Europe Daylight Time)"
```

### Converting Strings to Numbers

```javascript
Number("3.14")    // returns 3.14
Number(" ")       // returns 0
Number("")        // returns 0
Number("99 88")   // returns NaN

var y = "5";      // y is a string
var x = + y;      // x is a number

var y = "John";   // y is a string
var x = + y;      // x is a number (NaN)
```

### Converting Booleans to Numbers

```javascript
Number(false)     // returns 0
Number(true)      // returns 1
```

### Automatic Type Conversion

```javascript
5 + null    // returns 5         because null is converted to 0
"5" + null  // returns "5null"   because null is converted to "null"
"5" + 2     // returns "52"      because 2 is converted to "2"
"5" - 2     // returns 3         because "5" is converted to 5
"5" * "2"   // returns 10        because "5" and "2" are converted to 5 and 2
```

## JavaScript Type Conversion Table

Original Value	| Converted to Number	| Converted to String	| Converted to Boolean
--- | --- | --- | ---
false	| 0	| "false"	| false	
true	| 1	| "true"	| true	
0	| 0	| "0"	| false	
1	| 1	| "1"	| true	
"0"	| 0	| "0"	| true	
"000"	| 0	| "000"	| true	
"1"	| 1	| "1" |	true	
NaN	| NaN	| "NaN"	| false	
Infinity	| Infinity	| "Infinity"	| true	
-Infinity	| -Infinity	" | -Infinity"	| true	
""	| 0	| ""	| false	
"20"	| 20	| "20"	| true	
"twenty"	| NaN	| "twenty"	| true	
[ ]	| 0	| ""	| true	
[20]	| 20	| "20"	| true	
[10,20]	| NaN	| "10,20"	| true	
["twenty"]	| NaN	| "twenty"	| true	
["ten","twenty"]	| NaN	| "ten,twenty" | true	
function(){}	| NaN	| "function(){}"	| true	
{ }	| NaN	| "[object Object]"	| true	
null	| 0	| "null"	| false	
undefined	| NaN	| "undefined"	| false
