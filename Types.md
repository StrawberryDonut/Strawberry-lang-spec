# Variables

Variables of Strawberry language is a dynamic type variable so the type of a variable can be changed.

```js
a = 10
```
this code makes a variable named `a` that stores an int type value 10.   
You can assign to assigned variable again and also can assign a different type of value.
```js
b = 1
b = 2

b = "hello"
```

And you can also delete a variable using the keyword `del`.
```js
c = 3.14

del c
```

# Types

## int
Integer type of value store an integer number. There is no limit so you can store as big numbers as you want.   
With int, you can use following arithmetic operators: `+`, `-`, `*`, `/`, `%`, `**`

## float
Float type can store real numbers is much same as the int type except that float can store numbers below the decimal points.   
You can use following arithmetic operators: `+`, `-`, `*`, `/`, `%`, `**`

## bool
Boolean type can store only two values: `true` and `false`.   
You can use the logical operators with bool type.

## list
You can store different types of multiple values in a list.
```js
a = [1, true, 'Hello', [3.14, 'world']]
```

Some operators are available for the list type.
- `<list> '+' <list>`: Combines the two lists.
- `<list> '-' <list>`: Removes all elements of the second in the first.
- `<list> '*' <int> `: Multiplies the list.
    ```js
    [1, 2, 3] * 3 == [1, 2, 3, 1, 2, 3, 1, 2, 3]
    ```
- `<list> '/' <any> `: Splits the list.
    ```js
    [1, 2, 3, 4, 5] / 3 == [[1, 2], [4, 5]]
    ```

With following codes, you can get an element by the index.
```js
a = [1, 2, 3]

a[1] // 2

a[-1] // 3
```

Also, like python, you can use list slicing.
```js
a = [1, 2, 3, 4, 5]

a[0:3] // [1, 2, 3]

a[2:] // [3, 4, 5]

a[:4] // [1, 2, 3, 4]

a[:] // [1, 2, 3, 4, 5]
```

These are grammars for the codes above.
```
<list> '[' <int> ']'
```
```
<list> '[' <int>? ':' <int>? ']'
```

You can also read the list functions [here](Functions.md#list-functions)

## string
String type value stores texts.
```js
a = "Hello, world!"
b = 'wa sans'
```

You can use operators similar to the list.
- `<string> '+' <string>`: Combine two strings.
- `<string> '-' <string>`: Removes all second strings in the first.
- `<string> '*' <int>   `: Multiplies the string.
- `<string> '/' <string>`: Split the string.
    ```js
    'hello, world!' / ', ' // ['hello', 'world!']
    ```

String values are basically considered as a list of strings, so you can get a string of a single letter with `[]` or can get a string with slicing.
```js
s = 'Hello, world!'

s[3] // 'l'

s[-5] // 'o'

s[2:5] // 'llo'
```

You can read the string functions [here](FUnctions.md#string-functions)

## dic
Dictionary type has pairs of keys and values. The key must be a string type. You can access to a member with `[]` or `.`
```
a = {'first': 1, 'second': 'hello', 'third': false}

a['first'] // 1

a.second // hello
```

You can use `+` and `-` operators and it works as same as with the list.

You can read the dictionary functions [here](FUnctions.md#dictionary-functions)

## function
Functions are also considered as a type.

```go
func a() {

}
```
this code makes a function type variable `a`.   
With the following codes, you can make the Anonymous function with a lambda expression.
```js
a = () => {

}
```