# My Note

* 布尔类型的数组有以下几种写法：
    * boolean [] aa = new boolean[3];
    * 或者
    * boolean aa [] = new boolean[3];
    * 或者
    * boolean aa [] = new boolean[] { true, false ,true}
       *  前两个都没给数组元素赋初始值，默认都为false ，等价于{false, false ,false}
       *  boolean类型数组其实很好理解，就是说明数组的每一个元素都是boolean类型的（是true，或是是false）
     
     以第三个为例：aa[0] = true ;aa[1] = false ;aa[2] = true;

* 赋值运算符容易混乱的点：
   * 等号右边赋值给等号左边 A=B，则将B的值赋值给A。
