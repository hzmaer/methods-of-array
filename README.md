# methods-of-array
数组各种方法汇总

一.ECMAScript数组的每一项可以保存任何类型的数据

二.创建数组的基本方式有两种

第一种使用Array构造函数 var colors=new Array();

第二种使用数组字面量表示法 var colors=["red","blue","yellow"]

三.检测数组 if(Array.isArray(value)){

           //对数组执行某些操作
           
            }
            
四.所有对象都具有toLocaleString(),toString()和valueOf()方法

   调用数组的toString()方法会返回由数组中的每个值的字符串形式拼接而成的一个以逗号分隔的字符串
   
   但是调用valueOf()返回的还是数组
   
五.栈方法   push()方法可以接收任意数量的参数，把他们逐个添加到数组末尾，并返回修改后数组的长度。








           pop()方法则从数组末尾移除最后一项，减少数组的length值，然后返回移除的值。
   
