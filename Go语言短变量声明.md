# `var` 一般定义全局变量

```
// 定义一个名称为“variableName”，类型为"type"的变量
// var variableName type
var number int

// 初始化“variableName”的变量为“value”值，类型是“type”
// var variableName type = value
var number int = 10

/*
    定义三个类型都是"type"的变量,并且分别初始化为相应的值
    vname1为v1，vname2为v2，vname3为v3
*/
// var vname1, vname2, vname3 type = v1, v2, v3
var number1, number2, number3 int = 1, 2, 3

/*
    定义三个变量，它们分别初始化为相应的值
    vname1为v1，vname2为v2，vname3为v3
    然后Go会根据其相应值的类型来帮你初始化它们
*/
// var vname1, vname2, vname3 = v1, v2, v3
var number1, number2, number3 = 1, 2, 3
```

# `:=` 短变量声明

形式：

```
变量名 := 表达式
```

**变量类型根据表达式自动推导**

```
// 声明初始化一个变量
s := "hello"

// 声明初始化一组同类型变量
min, max := 1, 1000

// 声明初始化一组不同类型变量
a, b, c := 1.32, true, "你好"
```

短变量声明方式只能用于**函数内部的局部变量**，不能在函数外使用，在函数外声明变量，需要使用 `var` 语句。

短变量声明语句中**至少要声明一个新的**变量，否则直接使用赋值语句 `=` 就可以了。

在不同的作用域(if,for,switch)中，重复使用短变量声明时，如果变量名相同，会重新声明新的变量。
