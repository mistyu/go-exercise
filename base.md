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
```
## 基础数据类型
