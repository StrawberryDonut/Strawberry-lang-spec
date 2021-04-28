# StrawberryLang
Description of Strawberry Language


## Keywords
|      |      |      |        |        |
|------|------|------|--------|--------|
|break |case  |catch |continue|default |
|del   |else  |false |finally |for     |
|func  |if    |in    |null    |readonly|
|return|switch|true  |try     |while   |


## Operators
|                     |         |       |      |       |       |       |
|---------------------|---------|-------|------|-------|-------|-------|
|Arithmetic           |a + b    |a - b  |a * b |a / b  |a % b  |a ** b |
|Comparison           |a == b   |a != b |      |       |       |       |
|Relational           |a < b    |a > b  |a <= b|a >= b |       |       |
|Logical              |a \|\| b |a && b |!a    |       |       |       |
|Bitwise              |a & b    |a \| b |a ^ b |~a     |       |       |
|Shift                |a >> b   |a << b |      |       |       |       |
|Assignment           |a = b    |       |      |       |       |       |
|Arithmetic Assignment|a += b   |a -= b |a *= b|a /= b |a %= b |a **= b|
|Bitwise Assignment   |a &= b   |a \|= b|a ^= b|       |       |       |
|Shift Assignment     |a >>= b  |a <<= b|      |       |       |       |
|Increment & Decrement|a++      |a--    |++a   |--a    |       |       |
|Conditional          |a ? b : c|       |      |       |       |       |


## Types
|        |        |        |        |        |        |        |
|--------|--------|--------|--------|--------|--------|--------|
|int     |float   |bool    |string  |list    |dic     |function|


## Statements

### if
```
 'if'        '(' <bool> ')' '{' <statement>* '}'
('else' 'if' '(' <bool> ')' '{' <statement>* '}')*
('else'                     '{' <statement>* '}')?
```

### for
```
'for' '(' <int> ')' '{' <statement>* '}'
```

```
'for' '(' <identifier> 'in' <list> ')' '{' <statement>* '}'
```

### while
```
'while' '(' <bool> ')' '{' <statement>* '}'
```

### switch case
```
'switch' '(' <any> ')' '{'
    ('case'    '(' <any multiple> ')' '{' <statement>* '}')*
    ('default'                        '{' <statement>* '}')?
'}'
```

### try catch
```

```

### function
```
'func' <identifier> '(' <identifier multiple> ')' '{' <statement>* '}'
```

### comment
```
'//' CHAR* END_OF_LINE
```
```
'/*' CHAR* '*/'
```