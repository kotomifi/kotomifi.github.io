# python note
## range和xrange
> 在python中创建递增序列可以使用range或者xrange

```python
>>> x=xrange(0,8)
>>> print x
xrange(8)
>>> print x[0]
0
>>> print x[7]
7
```


> range()函数返回一个递增或递减的数字列表，列表的元素由三个参数决定：
> - start: 表示列表的开始值，默认为0
> - stop:  表示列表的结束值，不可缺少
> - step:  表示增长步长，默认为1

