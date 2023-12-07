# go 基础

## 基础知识
```go
// 定义一个变量
var name = 1
var name int
name := 1
// 定义了变量必须使用

var (
  name = "mistyu"
  age = 18
)

var name, age = "mistyu", 18

// 定义常量
const PI float32 = 3.1415926

const (
  x int = 16
  y // 16
  z = "abc"
  c // 'abc'
)

// iota 默认从 0 开始的枚举
const (
  x = iota
  y // 1
  z // 2
  c // 3
)

// iota 默认从 0 开始的枚举
const (
  x = iota + 1 // 1
  y // 2
  z = "mistyu"
  c // "mistyu"
  m // "mistyu"
  i // "mistyu"
  s = iota // 6
  t // 7
)
// 每次 const 都会初始化 iota


// 匿名变量
func a() (int, bool) {
  return 0, false
}
_r1, ok := a()
// 可以不使用 r1
if (ok) {
  // todo
}
```
## 基础数据类型
```go
/**
 * 整数类型
 */
int8 // 有符号 8 位整型(-128 到 127) 长度: 8bit
int16 // 有符号 16 位整型(-32768 到 32767)
int32 // 有符号 32 位整型(-2147483648 到 2147483647)
int64 // 有符号 32 位整型(-9223372036854775808 到 9223372036854775807)
uint8 // 无符号 8 位整型(0 到 255)
uint16 // 无符号 8 位整型(0 到 65535)
uint32 // 无符号 8 位整型(0 到 4294967295)
uint64 // 无符号 8 位整型(0 到 18446744073709551615)

/**
 * 浮点类型
 */
float32 // 32 位浮点型数
float64 // 64 位浮点型数

/**
 * 其他
 */
byte 等于 uint8 // 用于存放字符的 ACII 值
rune 等于 int32 // 用于存放字符如 汉子/日文/韩文等
```

### 类型转换
```go
var a int8 = 12
var b = uint8(a)

var f float32 = 3.14
var c = int32(f)

var f64 = float64(a)

// 字符串转数字
var str = "12"
myint, err := strconv.Atoi(str)
if err != nil {

}

// 数字转字符串
var myInt = 12
var str = strconv.Itoa(myInt)

// 字符串转 float32 、bool
strconv.ParseFloat("3.1415", 32)
strconv.ParseBool("true")
```

## 数组
### 切片
```go
var courses []string
courses = append(courses, "go")
courses = append(courses, "js")
courses = append(courses, "rust")
courses = append(courses, "dart")

// 初始化切片
// 1. 从数组直接创建
allCourses := []string{"go", "js", "rust", "dart"}
course1 := allCourses[0:2] // ["go", "js"]

// 2. 使用 string{}
courses2 := []string{"go", "js", "rust", "dart"}

// 3. make
courses3 := make([]string, 4)
courses3[0] = "go"


// 本质上是值传递
data := []int{1, 2, 3, 4, 5, 6, 7, 8, 9, 10}
a1 := data[1:6]
a2 := data[2:7]

// 扩容之后就会复制一份断开之前的引用
s2 := append(s2, 1, 2, 3,4 ,5 ,6, 7, 8, 9, 1, 1, 1)
s2[0] = 11

fmt.Println(s2) // [11, 4, 5, 6, 7, 8, 9, 1, 1, 1]
fmt.Println(s1) // [2, 3, 4, 5, 6]
```

## Map
```go
// 初始化一个map
map1 := map[string]string{}
map["go"] = "go map"

map2 := make(map[string]string, 3)
```

## List(链表)
```go
var myList list.List
```

## package
用来组织源码，是多个 go 源码的结合，代码复用的基础，fmt, os, io
每个源码文件开始都必须要申明所属的 package
