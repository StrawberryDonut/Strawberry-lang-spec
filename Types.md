# Variables

Variables of Strawberry language is a dynamic type variable so the type of a variable can be changed.

```js
a = 10
```
this code makes a variable named `a` that stores an int type value 10.   
You can assign to assigned variable again and also can assign a different type of value.
```js
a = 1
a = 2

a = "hello"
```

You can declare a variable as read-only by writing the keyword `readonly` in front of the name of the variable.
```cs
readonly a = 1

a = 2 // ERRrOR!
```

And you can also delete a variable using the keyword `del`.
```py
a = 3.14

del a
```

# Types

## int
Integer type of value store an integer number. There is no limit so you can store as big numbers as you want.   
With int, you can use following arithmetic operators: `+`, `-`, `*`, `/`, `%`, `**`

## float
Float type can store real numbers and it is similar to the int type except that float can store numbers below the decimal points.   
You can use following arithmetic operators: `+`, `-`, `*`, `/`, `%`, `**`

## bool
Boolean type can store only two values: `true` and `false`.   
You can use the [logical operators](Operators.md#logical-operators) with bool type.

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
    [1, 2, 3] * 3 // [1, 2, 3, 1, 2, 3, 1, 2, 3]
    ```
- `<list> '/' <any> `: Splits the list.
    ```js
    [1, 2, 3, 4, 5] / 3 // [[1, 2], [4, 5]]
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
You can use escape sequences: `\n`, `\t`, `\b`, `\r`. And you can use string format with `{}`.

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
a = 'Hello, world!'

a[3] // 'l'

a[-5] // 'o'

a[2:5] // 'llo'
```

You can read the string functions [here](FUnctions.md#string-functions)

## dic
Dictionary type has pairs of keys and values. The keys must be a string type. You can access to a member with `[]` or `.`
```js
a = {'first': 1, 'second': 'hello', 'third': false}

a['first'] // 1

a.second // hello
```

You can use `+` and `-` operators which work the same as with the list.

You can read the dictionary functions [here](FUnctions.md#dictionary-functions)

## function
Functions are also considered as a type.

```go
func a() {

}
```
this code makes a function-type variable `a`.   
With following codes, you can make the Anonymous function with a lambda expression.
```js
a = () => {

}
```
