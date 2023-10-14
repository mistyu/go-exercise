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
byte 等于 uint8
rune 等于 int32
```