# java笔记


## This关键字
* this是什么？看上去是用于区分局部变量和成员变量同名情况
* this：代表一个本类的对象，到底代表哪一个呢？	
    * this代表它所在函数所属对象的引用。
    * 哪个对象在调用this所在的函数，this就代表哪个对象。
      
* this的应用：
    * 当定义类中功能时，该函数内部要用到调用该函数的对象时，用this来显示这个对象
    * 但凡本类功能内部使用到了本类对象，都使用this表示。
      
* this语句
    * 用于构造函数之间相互调用。 

* **this语句只能定义在构造函数的第一行，因为初始化要先执行。**


## Static关键字
* 用法：是一个修饰符，用于修饰成员（成员变量，成员函数）
    * 当成员被静态修饰后，就多了一种调用方式，除了可以被对象调用外，还可以直接被类名调用。类名.静态成员

* 特有内容随着对象存储在堆内存当中，共有对象随着类存储的方法区

* static特点：
    * 1、随着类的加载而加载
         静态会随着类的消失而消失，生命周期最长   
    * 2、优先于对象存在
    * 3、被所有对象所共享
    * 4、可以被类名所调用
  
* 实例变量和类变量的区别：
    * 1.存放位置
          类变量随着类的加载而存在于方法区中，
          实例变量随着对象的建立而存在于堆内存中
    * 2.生命周期
         类变量生命周期最长，随着类的消失而消失。
         实例变量生命周期随着对象的消失而消失。
* 静态使用注意事项：
    * 1.静态方法只能访问静态成员。
      非静态方法既可以访温静态也可以访问非静态
    * 2.静态方法中不可以定义this，super关键字
       因为静态优先于对象存在，所以静态方法不可以出现this。
       
 * 静态的特点：
     * 1. 优点：对对象的共享数据进行单独空间的存储，节省空间，没有必要每一个对象中都存储一份
          可以直接被类名调用。
     * 2. 缺点：生命周期过长，访问出现局限性（静态虽然好，但只能访问静态）
     
  **什么时候使用静态**
  
* 从两方面下手（因为静态修饰的内容有成员变量和函数）
  * 什么时候定义静态变量（类变量）？
       
       当对象中出现共享数据时候（共享值），该数据被静态所修饰
       
       对象中的特有数据要定义成非静态存在于堆内存中
       
  * 什么时候定义静态函数？
  
      当功能内部没有访问到非静态数据（对象的特有数据）
  
      那么该功能都可以定义成静态函数
     


## 主函数
  public static void main(String[] args)
     主函数：是一个特殊函数。作为程序的入口，可以被JVM调用，具有固定格式
 * 定义：
	*  public：代表该访问权限是最大的
	*  static：代表主函数随着类的加载就已经存在了
   * void: 主函数没有具体的返回值
   *  main: 不是关键字，但是是一个特殊的单词，可以被JVM识别
   * （String[] args）：函数的参数，函数类型是一个数组，该数组中的元素是字符创，字符串类型的数组
      * 虚拟机调用函数时候，必须往里传入数据，不是数组类型就是NULL 利用DOS可以验证
      
 
**方法区即共享区、数据区**
对象一旦建立，属性就需要默认初始化，之后是构造代码块的初始化。
