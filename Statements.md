# Statements

[Home](README.md) |
Statements |
[Operators](Operators.md)

## if
```
 'if'        '(' <bool> ')' '{' <statement>* '}'
('else' 'if' '(' <bool> ')' '{' <statement>* '}')*
('else'                     '{' <statement>* '}')?
```

## for
```
'for' '(' <int> ')' '{' <statement>* '}'
```

```
'for' '(' <identifier> 'in' <list> ')' '{' <statement>* '}'
```

## while
```
'while' '(' <bool> ')' '{' <statement>* '}'
```

## switch case
```
'switch' '(' <any> ')' '{'
    ('case'    '(' <any multiple> ')' '{' <statement>* '}')*
    ('default'                        '{' <statement>* '}')?
'}'
```

## try catch
```

```

## function
```
'func' <identifier> '(' <identifier multiple> ')' '{' <statement>* '}'
```

## comment
```
'//' .* END_OF_LINE
```
```
'/*' .* '*/'
```