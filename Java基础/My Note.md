# My Note

## 布尔类型的数组有以下几种写法：
   * boolean [] aa = new boolean[3];
   * 或者
   * boolean aa [] = new boolean[3];
   * 或者
   * boolean aa [] = new boolean[] { true, false ,true}
      *  前两个都没给数组元素赋初始值，默认都为false ，等价于{false, false ,false}
      *  boolean类型数组其实很好理解，就是说明数组的每一个元素都是boolean类型的（是true，或是是false）
     
   * 以第三个为例：aa[0] = true ;aa[1] = false ;aa[2] = true;

## 赋值运算符容易混乱的点：
   * 等号右边赋值给等号左边 A=B，则将B的值赋值给A。
   * +=  int x-3 ; x+=4 相当于 x=x+4 
         * 但是有存在这一的区别 Short s=4;s=s+4 就是两次运算，加法的结果是整型，编译结果失败，
         而s+=4 做自动转换类型动作,S被提升为Int型

## DOS命令界面命令：
  C:\md xxx  创建文件夹
  
  C:\rd xxx  删除文件夹 必须保证该文件夹内为空
  
  C:\cd abc 进入目录
  
  C:\abc\dir 打开目录
  
  C:\abc\cd.. 返回上一层目录
  
  C:\abc\op\cd\ 直接返回到根目录
  
  del 删除文件，将会出现\*.是否确认<Y/N>?
  
  exit 推出DOS命令行


  ## 转移字符
   * \n 换行
   * \b 退格 
   * \r 按下回车键 回车符是 由\r\n 表示
   * \t 制表符 相当于tab键

## JAVA 关键字的学习
### 迭代器（Iterator）
  *　迭代器是一种设计模式，它是一个对象，它可以遍历并选择序列中的对象，而开发人员不需要了解该序列的底层结构。迭代器通常被称为“轻量级”对象，因为创建它的代价小。 
   *    Java中的Iterator功能比较简单，并且只能单向移动  
   *　  (1) 使用方法iterator()要求容器返回一个Iterator。第一次调用Iterator的next()方法时，它返回序列的第一个元素。
   
   注意：iterator()方法是java.lang.Iterable接口,被Collection继承。     
   
 　*　　(2) 使用next()获得序列中的下一个元素。
     
   *　　(3) 使用hasNext()检查序列中是否还有元素。
     
   *　　(4) 使用remove()将迭代器新返回的元素删除。
     
   *　  Iterator是Java迭代器最简单的实现，为List设计的ListIterator具有更多的功能，它可以从两个方向遍历List，也可以从List中插入和删除元素。
