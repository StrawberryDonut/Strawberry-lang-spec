# Built In Functions

## type casts

### int()
`int(<float|string> value) -> <int>`   
Converts `value` to int.
```js
int(3.14) // 3

int('123') // 123
```

### float()
`float(<int|string> value) -> <float>`   
Converts `value` to float.
```js
float(1) // 1.0

float('3.14') // 3.14
```

### bool()
`bool(<int> value) -> <bool>`   
Converts `value` to bool. negative number or `0` return `false`, positive number returns `true`.
```js
bool(1) // true
bool(-10) //false
```

### string()
`string(<int|float|bool|list|dic|function> value) -> <string>`   
Converts `value` to string.
```js
string(1) // '1'

string(3.14) // '3.14'

string(true) // 'true'

string([1, true, 'hello']) // '[1, true, \'hello\']'

string({'a': 1, 'b': 2}) // '{\'a\': 1, \'b\': 2}'

string((a) => { print(a) }) // 'function (a)'
```

### list()
`list(<dic> value) -> <list>`   
Converts `value` to list.
```js
list({'a': 1, 'b': 2}) // [['a', 1], ['b', 2]]
```

### dic()
`dic(<list> value) -> <dic>`   
Converts `value` to dic.
```js
dic(['hell', 'o', 'world']) // {'0': 'hell', '1': 'o', '2': 'world'}
```

## default functions

### type()
`type(<any> value) -> <string>`   
Get type of a `value` as string.
```js
type(1) // int

type('hello') // string

type({'a': 1}) // dic

type(() => {}) // function
```

### random()
`random(<int|float> x?, <int|float> y) -> <int|float>`   
Return random value between `x` and `y`. `x` is inclusive and `y` is exclusive.
```js
random(1, 3.14) // 2.1
```

### range()
`range(<int> start?, <int> end, <int> step?) -> <list>`   
Return a list of numbers starts from `start` (`0` for default) to `end` (exclusive)
```js
range(10) // [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

range(0, 20, 2) // [0, 2, 4, 8, 10, 12, 14, 16, 18]
```

### time()
`time() -> <dic>`   
Get current UTC time with following format:  
```
{'timestamp': n, 'year': yyyy, 'month': MM, 'day': dd, 'hour': HH, 'minute': mm, 'second': ss}
```

### numberToUnicode()
`numberToUnicode(<int> code) -> <string>`

### unicodeToNumber()
`unicodeToNumber(<string> unicode) -> <int>`

## math functions


# Member Functions

## string functions


## list functions


## dictionary functions


# Story Functions