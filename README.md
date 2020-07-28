# daka_04_list

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
