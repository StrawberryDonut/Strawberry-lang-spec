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

### choice()
`random(<list>) -> <any>`   
Return a random element in the list.

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

### replace()
`<string>.repalce(<string> old, <string> new) -> <string>`   
Change all `old` strings into `new` string.
```js
'Hello, world!'.repalce('o', 'asdf') // 'Hellasdf, wasdfrld!'
```

### indexOf()
`<string>.indexOf(<string> value) -> <int>`  
Return an index of `value`.
```js
'Hello, world!'.indexOf('ll') // 2

'Wa, sans!'.indexOf('papyrus') // -1
```

### toUpper()
`<string>.toUpper() -> <string>`   
Makes a string to upper case.

### toLower()
`<string>.toLower() -> <string>`   
Makes a string to lower case.

### isUpper()
`<string>.isUpper() -> <bool>`   
Check if a string is upper case.

### isLower()
`<string>.isLower() -> <bool>`   
Check if a string is lower case.

### startsWith()
`<string>.startsWith(<string> value) -> <bool>`   
Check if a string starts with `value`.

### endsWith()
`<string>.endsWith(<string> value) -> <bool>`   
Check if a string ends with `value`.

### trim()
`<string>.trim() -> <string>`   
Remove whitespace from the start and end of a string.

### trimLeft()
`<string>.trimLeft() -> <string>`   
Remove whitespace from the start of a string.

### trimRight()
`<string>.trimRight() -> <string>`   
Remove whitespace from the end of a string.

### length()
`<string>.length() -> <int>`   
Return the length of string.

## list functions

### join()
`<list>.join(<string|list> separator) -> string`   
Joins the list with `separator`.
```js
[1, 2, 3].join(', ') // '1, 2, 3'

[2021, 04, 29, 19, 22, 20].join(['년 ', '월 ', '일 ', '시 ', '분 ', '초']) // 2021년 04월 29일 19시 22분 20초
```

### indexOf()
`<list>.indexOf(<any> element) -> <int>`  
Return an index of `element`.
```js
[1, 2, 3].indexOf(2) // 1

[4, 5, 6].indexOf(7) // -1
```

### reverse()
`<list>.reverse() -> <list>`   
Return a reversed list.
```js
[1, 2, 3].reverse() // [3, 2, 1]
```

### sort()
`<list>.sort() -> <list>`   
Return a sorted list.
```js
[2, 3, 1].sort() // [1, 2, 3]
```

### pop()
`<list>.pop() -> <any>`   
Remove the last element and return it.
```js
a = [1, 2, 3]
a.pop() // 3
// a == [1, 2]
```

### add()
`<list>.add(<any> value) -> <list>`   
Add `value` to the list and return the list.
```js
a = [1, 2, 3]
a.add(4) // [1, 2, 3, 4]
// a == [1, 2, 3, 4]
```

### remove()
`<list>.remove(<int> index) -> <list>`   
Remove an element of `index` in the list and return the list.
```js
a = [1, 2, 3]
a.remove(1) // [1, 3]
// a == [1, 3]
```

### length()
`<list>.length() -> <int>`   
Return the length of list.

### get()
`<list>.get(<function> condition) -> <list>`   
Find all elements that function `condition` return `true`. The function must have only one argument.
```go
a = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
func b(i) {
    return i % 2 == 0
}
a.get(b) // [2, 4, 6, 8, 10]

a.get((i) => i % 3 == 0) // [3, 6, 9]
```

### set()
`<list>.set(<function> selector) -> <list>`   
Return a new list that all elements changed by `selector`. The function must have only one argument.
```go
a = [1, 2, 3, 4, 5]
func b(i) {
    return i * 2
}
a.set(b) // [2, 4, 6, 8, 10]

a.set((i) => i * 3) // [3, 6, 9, 12, 15]
```

## dictionary functions

### keys()
`<dic>.keys() -> <list>`   
Return a list that contains all key.

### values()
`<dic>.values() -> <list>`   
Return a list of all values.

### has()
`<dic>.has(<string> key) -> <bool>`   
Check if there is a key named `key`.

### delete()
`<dic>.delete(<string> key) -> <dic>`   
Remove a value with `key` and return the dictionary.

### length()
`<dic>.length() -> <int>`   
Return the length of a dictionary.

### get()
`<dic>.get(<function> condition) -> <list>`   
Find all elemts that function `condition` return `true`. The function must have two argument (key, value).
```js
{'a': 1, 'b': 2, 'c': 3}.get((k, v) => v % 2 == 1) // {'a': 1, 'c': 3}
```

### set()
`<dic>.set(<function> selector) -> <dic>`   
Return a new list that all elements changed by `selector`. THe function must have two argument (key, value).
```js
{'a': 1, 'b': 2, 'c': 3}.set((k, v) => {k * 2, v * 2}) // [{'aa': 2, 'bb': 4, 'cc': 6}]
```

# Story Functions

## default story functions

### img()
`story.img(<string> url) -> <null>`   
Set image of the message.

### addField()
`story.addField(<string> name, <string> value, <bool> inline = false) -> <null>`   
Add embed field to the message.

### addReaction()
`story.addReaction(<string> name) -> <null>`   
Add built-in emojis of Discord to the message.

`story.addReaction(<int> id) -> <null>`   
Add custom server emoji to the message.

### setContent()
`story.setContent(<string> content) -> <null>`   
Set content of the message.

### input()
`story.input(<string> text = "입력 대기중...", <function> event) -> <null>`   
Get user input.
```go
func onInputReceived(msg) {
    
}

story.input("Enter a message...", onInputReceived)
```

### randomUser()
`story.randomUser() -> <dic>`   
Get a random user in current Discord server.

## data functions

### set()
`story.set(<string> key, <any> value) -> <null>`   
Save a value in the server.

### get()
`story.get(<string key>) -> <any>`   
Load a value from the server.

### exist()
`story.exist(<string> key) -> <bool>`   
Check if the key exists.

### delete()
`story.delete(<string> key) -> <any>`
Remove a value from the server.
