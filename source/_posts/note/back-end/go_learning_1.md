---
title: Go语言初上手(一) 基础语法
link: back-end/go/go_learning_1
catalog: true
lang: cn
date: 2022-05-05 19:51:01
subtitle: go语言基本语法，与c++和JS的区别与类似点
cover: img/header_img/95694792_p0.jpg
tags:
- Go
categories:
- [笔记, 后端]
---

# 安装 Go 语言
> 1. 访问 https://go.dev/ ，点击 Download ，下载对应平台安装包，安装即可
> 2. 如果无法访问上述网址，可以改为访问 https://studygolang.com/dl 下载安装
> 3. 如果访问 github 速度比较慢，建议配置 go mod proxy，参考 https://goproxy.cn/ 里面的描述配置，下载第三方依赖包的速度可以大大加快

# 基础数据类型

# 程序结构
https://books.studygolang.com/gopl-zh/ch2/ch2.html

## 声明与变量

### var
一般语法如下

```go
var 变量名 类型 = 表达式
```
类型省略则根据表达式自动推导，如果表达式为空，则用 **零值** 初始化该变量（因此在Go语言中**不存在未初始化的变量**）

| 类型 | 零值 |
| ---- | ---- |
| 数值 | `0` | 
| 布尔 | `false` | 
| 字符串 | "" |
| 数组或结构体等聚合类型 | `nil` |  

可以在一个声明语句中同时声明一组变量，或用一组初始化表达式声明并初始化一组变量。

```go
var i, j, k int     // int int int
var b, f, s = true, 2.3, "hello" // bool float64 string
```

一组变量也可以通过调用一个函数，由函数返回的多个返回值初始化：

```go
var f, err = os.Open(name) // os.Open returns a file and an error
```
### 简短变量声明 `:=`

以`名字 := 表达式`的形式声明变量，变量的类型根据表达式来自动推导
- 因为其简洁和灵活的特点，简短变量声明被广泛用于大部分的局部变量的声明和初始化。
- 而var形式的声明语句往往是用于需要显式指定变量类型的地方，或者因为变量稍后会被重新赋值而初始值无关紧要的地方。

```go
i := 100                  // int
i, j := 0, 1              // int int
var boiling float64 = 100 // a float64
var names []string
var err error
```

- 简短变量声明语句对在同级词法域已经声明过的变量只会进行赋值行为
- 如果变量是在外部词法域声明的，那么简短变量声明语句将会在当前词法域重新声明一个新的变量

### 指针
与c语言中类似，通过 `&`操作符取址，通过 `*` 取值
```go
x := 1
p := &x         // p, of type *int, points to x
fmt.Println(*p) // "1"
*p = 2          // equivalent to x = 2
fmt.Println(x)  // "2"
```
任何类型的指针的零值都是 `nil`。
- 若`p`指向某个有效变量，那么 `p != nil` 测试为真。
- 当两指针指向同一个变量或全部是 `nil` 时才相等。

### `new` 函数
`new(T)` 将创建一个 `T` 类型的匿名变量，初始化为 `T类型的零值`，然后返回变量地址，返回的指针类型为 `*T`。
- Go 语言中的`new`是个预定义的**函数**，不是关键字！所以可以重新定义。
```go
p := new(int)   // p, *int 类型, 指向匿名的 int 变量
fmt.Println(*p) // "0"
*p = 2          // 设置 int 匿名变量的值为 2
fmt.Println(*p) // "2"
```

## 类型 `type`
类似于c++中的typeof的加强版，形式如下
```go
type 类型名 底层类型
```
如下，声明了两种类型：`Celsius` 和 `Fahrenheit` 分别对应不同的温度单位。
- 底层数据类型决定其内部结构和表达方式
- 它们虽然有着相同的底层类型 `float64`，但是它们是不同的数据类型，因此它们**不可以被相互比较或混在一个表达式运算。**
- 类型转换不会改变值本身，但是会使它们的语义发生变化。
```go
import "fmt"

type Celsius float64    // 摄氏温度
type Fahrenheit float64 // 华氏温度

const (
    AbsoluteZeroC Celsius = -273.15 // 绝对零度
    FreezingC     Celsius = 0       // 结冰点温度
    BoilingC      Celsius = 100     // 沸水温度
)

func CToF(c Celsius) Fahrenheit { return Fahrenheit(c*9/5 + 32) }

func FToC(f Fahrenheit) Celsius { return Celsius((f - 32) * 5 / 9) }
```

比较运算符==和<也可以用来比较一个命名类型的变量和另一个有相同类型的变量，或有着相同底层类型的未命名类型的值之间做比较。但是如果两个值有着不同的类型，则不能直接进行比较：

```go
var c Celsius
var f Fahrenheit
fmt.Println(c == 0)          // "true"
fmt.Println(f >= 0)          // "true"
fmt.Println(c == f)          // compile error: type mismatch
fmt.Println(c == Celsius(f)) // "true"! 类型转换操作不会改变值
```

命名类型还可以为该类型的值定义新的行为。这些行为表示为一组关联到该类型的函数集合，我们称为**类型的方法集** (在第六章会详细讲)

下面的声明语句，Celsius类型的参数c出现在了函数名的前面，表示声明的是Celsius类型的一个名叫String的方法，该方法返回该类型对象c带着°C温度单位的字符串：

```go
func (c Celsius) String() string { return fmt.Sprintf("%g°C", c) }
```

许多类型都会定义一个String方法，因为当使用fmt包的打印方法时，将会优先使用该类型对应的String方法返回的结果打印

```go
c := FToC(212.0)
fmt.Println(c.String()) // "100°C"
fmt.Printf("%v\n", c)   // "100°C"; no need to call String explicitly
fmt.Printf("%s\n", c)   // "100°C"
fmt.Println(c)          // "100°C"
fmt.Printf("%g\n", c)   // "100"; does not call String
fmt.Println(float64(c)) // "100"; does not call String
```
## 包和文件
## 作用域