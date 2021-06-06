这是标题
=======
# static-server
```function fn1() {
      var a = 2

      function fn2() {
        a++
        console.log(a)
      }
      return fn2;
    }
    var f = fn1();   //执行外部函数fn1，返回的是内部函数fn2
    f() // 3       //执行fn2
    f() // 4       //再次执行fn2```
