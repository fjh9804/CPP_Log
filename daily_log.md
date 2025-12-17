# 学习日志



### DAY1

```typescript
/*内联函数*/
1.内联函数体内不能有循环语句和switch语句；
2.内联函数的定义必须出现在内联函数第一次被调用之前；
3.对内联函数不能进行/*异常接口声明*/
```

### DAY2

```typescript
/*new和delete*/
new的行为＝申请内存＋构造对象
delete的行为＝调用析构函数＋释放内存
delete只能用于new生成的对象
delete后指针仍然存在，但已悬空，须手动置空

/*struct和class*/
区别在于 默认规则＋设计语义：
struct强调是一个数据结构，class强调是一个对象有固定的行为方法
数据->struct, 对象->class
```

### DAY3

```typescript
/*CMakeList语法*/
cmake_minimum_required(VERSION *.*)
project(工程名)

set(CMAKE_CXX_STAMDARD **)

//指定头文件所在目录
include_directories(文件夹名)
…如需多个目录，同上

//列出所有的源文件
file(GLOB_RECURSE SOURCES "文件夹/*.cpp" "*.cpp" etc.)

//生成可执行文件
add_executable(可执行文件名 ${SOURCES})
```

### DAY4

```typescript
/*Python与C/C++在语言哲学和工程上的差异映射*/
Python是一门“动态、解释、强运行时、弱类型约束、强抽象能力”的工程脚本语言

1.复杂性 从 编译器 推迟到了 运行期

2.变量无类型，对象有类型 变量只是一个“引用”

3.堆对象 引用计数＋GC 无指针运算 无显式释放 //几乎一切都是 “对象+引用”

4.无函数签名约束，参数可变，可返回多个值

5.控制结构，没有{}，用缩进定义作用域，强制代码结构清晰，for循环不是 控制变量，而是 遍历对象

6.容器 直接拉开效率差距 dict ~= C++ unordered_map+巨量优化
  配置表/参数表/JSON 映射在Python中几乎是“原生形态”

7.面向对象：比C++更彻底，函数、类、模块等都是对象，可以在运行期修改类、函数行为

8.异常模型：不是返回值 错误是 “异常路径”

9.性能观念：少写循环 多用库(C实现) 结构比算法重要

10.适合当前用途：配置表解析 代码生成 日志分析 自动化 测试 工具脚本


/*C++语法点*/
1.default用法

2.函数体前的const声明

3.is_empty()语法糖

4.std::cin/std::cout 级联输入输出时的先后顺序
```