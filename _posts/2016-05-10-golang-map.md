# Golang map
在C++/Java中，map都是以库函数的方式提供，而go语言不需要引入任何库，可以直接使用。

## 定义和创建
    // 定义一个map
    var myMap map[string]string 
    // 创建map
    myMap = make(map[string]string)
    // 创建时指定容量
    myMap = make(map[string]string, 100)
    // 创建并初始化
    myMap = map[string] "value"
    // 直接创建
    m := make(map[string]string)

