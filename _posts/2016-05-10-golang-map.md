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
    myMap = map[string] string {
        "a": "aa",
        "b": "bb",
    }
    // 直接创建
    m := make(map[string]string)


## 查找键值是否存在
    if v, ok := m1["a"]; ok {
        fmt.Println("key a exist")
    } else {
        fmt.Println("key a not exist")
    }

## 遍历map
    for k, v := range m1 {
        fmt.Println(k, v)
    }

## 获取长度
    // map只有长度，没有容量，因为map可以无限添加
    c := len(m1)

## map参数
map做为参数时，传递的是指针，而不是值，因此使用map的成本很低

## 并发
map不是线程安全的，如果要在多个线程中使用同一个map，需要自己加锁控制并发问题。
