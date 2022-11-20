## Introduction Basic
---
Cmake 是非常值得学习的编译生成工具，在最近的使用过程中发现，现代cmake的很多写法发生了很大的变化，所以跟着[An Introduction to Modern CMake](https://cliutils.gitlab.io/modern-cmake/)重新学习一下<br>

### Basic
1. minimum version
        从cmake3.12开始，VERSION支持范围式的定义<br>
```cmake
    cmake_minimum_require(VERSION 3.10...3.24)

    if (${CMAKE_VERSION} VERSION_LESS 3.24)
        cmake_policy(VERISON ${CMAKE_MAJOR_VERSION}.${CMAKE_MINOR_VERSION})
    else()
        cmake_policy(VERSION 3.24)   
    endif()
```
2. make library<br>
        add_library(name STATIC .cpp)<br>

### Variables and Cache

1. local variable<br>
        cmake中局部变量可以使用set(var "string")表示, 使用变量${var}
        cmake中变量list([operator] var arg) 当然可以使用set(mylist "one,two")
2. cache variable<br>
        如果想在输入命令时设置变量 可以使用 **cmake -L** 来显示所有的变量, 如果变量名是bool类型，可以使用快捷操作**option()**，所有的变量保存在CMakeCache.txt中
```cmake
        set(MYVAR "value" CACHE STRING "Description") #不会替换已有的变量
        mark_as_advanced(MYVAR)
        option(MYOPTION "ASDASD" ON/OFF)
```  
3. Properies
```cmake
    set_property(TARGET TargetName
             PROPERTY CXX_STANDARD 11)

    set_target_properties(TargetName PROPERTIES
                      CXX_STANDARD 11)
    get_property(ResultVariable TARGET TargetName PROPERTY CXX_STANDARD)

```
### Control flow   
cmake 中可以使用控制流来进行编程
```cmake
        if(statment)
        else()
        endif()
```
### Configure file
cmake可以通过配置文件获得相关变量的设置，这类配置文件在cmake中一般都是.in结尾<br>
```cmake
example.h.in 文件
#pragma once
#define MY_VERSON_MAJOR @PROJECT_VERSION_MAJOR@
example.h 文件
configure_file("${PROJECT_SOURCE_DIR}/include/example.h.in" "${PROJECT_BINARY_DIR}/include/example.h")


```




        









