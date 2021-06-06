
定义：
===
闭包就是能够读取其他函数内部数据（变量/函数）的函数。只有函数内部的子函数才能读取局部变量，因此可以把闭包简单理解成"定义在一个函数内部的函数"。        
作用：
===
作用1. 使用函数内部的变量在函数执行完后, 仍然存活在内存中(延长了局部变量的生命周期)，      
作用2. 让函数外部可以操作(读写)到函数内部的数据(变量/函数)        
举例子：
-------      
```    
     function fn1() {
      var a = 2

      function fn2() {
        a++
        console.log(a)
      }
      return fn2;
    }

    var f = fn1();   //执行外部函数fn1，返回的是内部函数fn2
    f() // 3       //执行fn2
    f() // 4       //再次执行fn2
```
作用1分析：上方代码中，外部函数fn1执行完毕后，变量a并没有立即消失，而是保存在内存当中。       
作用2分析：函数fn1中的变量a，是在fn1这个函数作用域内，因此外部无法访问。但是通过闭包，外部就可以操作到变量a。    
达到的效果是：外界看不到变量a，但可以操作a。
