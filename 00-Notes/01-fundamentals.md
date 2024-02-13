# Fundamentals - Part 1

---

## Values and Variables
- `value` is a piece of data
- we can store values in `variables`
- naming convention
    - camelCase
    - cannot start with number
    - can only contains numbers, letters, underscores, or the dollar sign
    - all in uppercase for constant
    - use descriptive variables

## Data Types
> - JavaScript has dynamic typing: We do **not** have to manually define the data type of the value stored in a variable. Instead, data types are determined **automatically**.  
> - We can assign a new value with a different data type to the same variable.
> - typeof null = object

- Primitive Type
    - Number
    - String
    - Boolean
    - Undefined
    - Null
    - Symbol (ES2015)
        - value that is unique and cannot be changed (not useful for now)
    - BigInt (ES2020)
        - large integers than the Number type can hold

- Reference Type
    - Object
    - Array
    - Function

## let, const, and var
四個不同：
1. 在作用域上，var 可以是全域、也可以是以函式作為範圍；let 與 const 則是以區塊作為範圍。
2. 在宣告上，var 可以被重複宣告，但是 let 與 const 則不行。
3. 在提升上，var 宣告的變數會自動初始化值為 undefined，因此在宣告前就使用變數，不會出現錯誤，而會是 undefined ；但是 let 與 const 宣告的變數則不會自動初始化，而是會進到暫時死區 (TDZ)，因此在 let 與 const 宣告變數前使用該變數，會出現錯誤。
4. let 與 const 在絕多數面向都是一樣，兩者的一大區別在於，用 let 宣告的變數可以重新賦值，但是用 const 的不行。

## Basic Operators
- Operators
    - Math Operators
    - Assignment Operators
    - Comparison Operators

- Precedence
    - [MDN](https://developer.mozilla.org/zh-TW/docs/Web/JavaScript/Reference/Operators/Operator_precedence)

## Strings and Template Literals
- use backticks ``
- multiline string
    ```javascript
    // before ES6
    'strings with \n\
    multiple \n\
    lines'

    // using backticks
    `String
    multiple
    line`
    ```

## if / else Statements
- control structure

## Type Conversion and Coercion
- Conversion 手動轉型、Coercion 強制轉型
- string`+`number 會把 number 轉為 string
- string`-`number 會把 string 轉為 number

## Truthy and Falsy Values
- falsy values
 - not false, but will be false when converted to boolean
 - 5 falsy values: 0, "", undefined, null, NaN
 - `Boolean({})` is `true`!


## Equality Operators: == vs. ===
- `==` 在比較兩個值之前，會先強制轉換型別與值，`===` 不會
- 有兩個例外情況
    - 比較 +0 和 -0時，嚴格比較會回傳 true
    - 比較 NaN 和 NaN 會是 false
- `Object.is()`
    ```javascript
    console.log(Object.is(+0, -0)); // false
    console.log(Object.is(NaN, NaN)); // true
    ```

## Boolean Logic
- AND

    |  AND   | True  | False |
    |  ----  | ----  | ----  |
    | True   | True  | False |
    | False  | False | False |

- OR

    |  OR    | True  | False |
    |  ----  | ----  | ----  |
    | True   | True  | True  |
    | False  | True  | False |


## Logical Operators
- AND: &&
- OR: ||
- NOT: !

## The Switch Statement

```javascript
switch(variable) {
    case 'value1':
        // ...
        break;
    case 'value2':
        // ...
        break;
    default:
        // ...
}
```

## Statements and Expressions
- An expression is any valid unit of code that resolves to a value
- 陳述式 (Statements) 一定會執行一些動作，但是不會回傳值或結果，常見的陳述式像是：
    - 流程控制 (Control flow)：if…else, switch, break
    - 變數宣告 (Declarations)： var, let, const
    - 函式宣告與類別 (Functions and classes)：function, async function, return, class
    - 迭代 (Iteration)：for, do…while, for…in, for…of, while
    - 其他：debugger, export, import, label

## The Conditional (Ternary) Operator

```javascript
 condition ? exprIfTrue : exprIfFalse
```
