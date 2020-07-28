# daka_04_list

列表

列表

1.列表的定义和创建
    中括号 []，逗号 ,
  
    x = [2, 3, 4, 5, 6, 7]
    print(x, type(x))
    #[2, 3, 4, 5, 6, 7] <class 'list'>
  
    利用range()创建列表
    x = list(range(1, 11, 2))
    print(x, type(x))
    #[1, 3, 5, 7, 9] <class 'list'>
    
    利用推导式创建列表
    x = [i for i in range(100) if (i % 2) != 0 and (i % 3) == 0]
    print(x, type(x))
    #[3, 9, 15, 21, 27, 33, 39, 45, 51, 57, 63, 69, 75, 81, 87, 93, 99] <class 'list'>
  
    创建一个混合列表
    mix = [1, 'lsgo', 3.14, [1, 2, 3]]
    print(mix, type(mix))  
    [1, 'lsgo', 3.14, [1, 2, 3]] <class 'list'>

    创建一个空列表
    empty = []
    print(empty, type(empty))  # [] <class 'list'>
  
2.向列表中添加元素

    list.append(obj)在列表末尾添加新的对象，只接受一个参数，参数可以是任何数据类型，被追加的元素在 list 中保持着原结构类型
    list.extend(seq)在列表末尾一次性追加另一个序列中的多个值（用新列表扩展原来的列表）
    list.insert(index, obj) 在编号 index 位置插入 obj

3.删除列表中的元素

    list.remove(obj) 移除列表中某个值的第一个匹配项
    list.pop([index=-1]) 移除列表中的一个元素（默认最后一个元素），并且返回该元素的值
    remove 和 pop 都可以删除元素，前者是指定具体要删除的元素，后者是指定一个索引。
    del var1[, var2 ……] 删除单个或多个对象。
    如果你要从列表中删除一个元素，且不再以任何方式使用它，就使用del语句；如果你要在删除元素后还能继续使用它，就使用方法pop(
        
4. 获取列表中的元素

    x = ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday']
    print(x[0], type(x[0]))  
    #Monday <class 'str'>
    print(x[-1], type(x[-1])) 
    #['Thursday', 'Friday'] <class 'list'>
    print(x[-2], type(x[-2]))  
    #Wednesday <class 'str'>
    print(x[3:])  
    #['Thursday', 'Friday']
    print(x[-3:])  
    #['Wednesday', 'Thursday', 'Friday']
    print(week[:3])  
    #['Monday', 'Tuesday', 'Wednesday']
    print(week[:-3])  
    #['Monday', 'Tuesday']
    print(week[1:3])  
    #['Tuesday', 'Wednesday']
    print(week[-3:-1])  
    #['Wednesday', 'Thursday']
    print(week[1:4:2])  
    #['Tuesday', 'Thursday']
    print(week[:4:2])  
    #['Monday', 'Wednesday']
    print(week[1::2])  
    #['Tuesday', 'Thursday']
    print(week[::-1])  
    #['Friday', 'Thursday', 'Wednesday', 'Tuesday', 'Monday']

5. 列表的常用操作符

    等号操作符：==
    连接操作符 +
    重复操作符 *
    成员关系操作符 in、not in

6. 列表的其它方法

    list.count(obj) 统计某个元素在列表中出现的次数
    list.index(x[, start[, end]]) 从列表中找出某个值第一个匹配项的索引位置
    list.reverse() 反向列表中元素
    list.sort(key=None, reverse=False) 对原列表进行排序。
    x = [123, 456, 789, 213]
    x.sort()
    print(x)
    #[123, 213, 456, 789]
    x.sort(reverse=True)
    print(x)
    #[789, 456, 213, 123]
    
    #获取列表的第二个元素
    def takeSecond(elem):
    return elem[1]
    x = [(2, 2), (3, 4), (4, 1), (1, 3)]
    x.sort(key=takeSecond)
    print(x)
    #[(4, 1), (2, 2), (1, 3), (3, 4)]
    x.sort(key=lambda a: a[0])
    print(x)
    #[(1, 3), (2, 2), (3, 4), (4, 1)]

7.练习题：

    1)、列表操作练习
    lst = [2, 5, 6, 7, 8, 9, 2, 9, 9]

    在列表的末尾增加元素15
        lst.append(15)

    在列表的中间位置插入元素20
        lst.insert(round(len(lst)/2),20)

    将列表[2, 5, 6]合并到lst中
        lst1 = [2, 5, 6]
        lst += lst1
    移除列表中索引为3的元素
        lst.pop(3)
    翻转列表里的所有元素
        lst.reverse()
    对列表里的元素进行排序，从小到大一次，从大到小一次
        lst.sort() "<"
        lst.sort(reverse=True)">"

8.总结

    列表有点像线性代数里的向量空间，C语言的数组，但是扩大了定义范围，可以对列表里的元素做各种操作。
