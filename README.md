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
           
六.队列方法 shift()方法能够移除数组中的第一个，将数组的长度减1,并且返回该项。    

           unshift()方法能在数组前端添加任意个项并返回新数组的长度。
           
七.重排序方法     reverse()方法会反转数组项的顺序
                
                比较函数  升序：function compare(){
                              if(value1<value2){
                                return -1;
                              }else if(value1>value2){
                                return 1;
                              }else{
                                return 0;
                              }
                              }
                              
                              eg.  var values=[0,1,5,10,15]
                                   values.sort(compare);
                                   console.debug(values) [0,1,5,10,15]
               
八.操作方法
   contact()方法可以基于当前数组中的所有项创建一个新数组
   
   slice()方法能够基于当前数组中的一或多个项创建一个新数组
   
   splice()方法的主要用途是向数组的中部插入项
   
九. 位置方法 indexOf()和lastIndexOf()。

            这两个方法都返回要查找的项在数组中的位置，或者在没有找到的情况下返回-1。
            
            indexOf()方法从数组的开头位置（0）开始向后查找，lastIndexOf()方法则从数组的末尾开始向前查找。
            
十. 迭代方法：传入这些方法中的函数会接收三个参数：数组项的值item，该项在数组中的位置index，数组对象本身array
    
    every() 对数组中的每一项运行给定函数，如果该函数对每一项都返回true,则返回true
    some()  对数组中的每一项运行给定函数，如果该函数对任意一项都返回true,则返回true
    filter()对数组中的每一项运行给定函数，返回该函数会返回true的项组成的数组
    map()   对数组中的每一项运行给定函数，返回每次函数调用的结果组成的数组
    forEach()对数组中的每一项运行给定函数，这个方法没有返回值，它只是对数组中的每一项运行传入的函数。
            这个方法没有返回值，本质上与使用for循环迭代数组一样。
            
十一.归并方法： reduce()和reduceRight()。这两个方法都会迭代数组的所有项，然后构建一个最终返回的值。
               reduce()方法从数组的第一项开始，逐个遍历道最后而reduceRight()则从数组的最后一项开始，向前遍历道第一项。
               这两个方法都接收两个参数：一个在每一项上调用的函数（必选）和作为归并基础的初始值。
              传给reduce()和reduceRight()的函数接收4个参数：前一个值，当前值，项的索引和数组对象。
              这个函数返回的任何值都作为第一个参数自动传给下一项。
              var values=[1,2,3,4,5]
              var sum=values.reduce(function(prev,cur,index,array){
                  return prev+cur;
              });
              alert(sum);
    
            
             
