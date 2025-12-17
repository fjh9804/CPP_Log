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