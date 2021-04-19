SocketWrite0和SocketRead0分析

这两个函数的栈回朔信息中可以看到，
最上层的函数是 java.lang.Thread.run(Thread.java 764) 中。

java.net.SOcketOutputStream.socketWrite0(Native Method)
java.net.SocketOutputStream.socketWrite
java.net.SocketOutputStream.write
com.example.okhttp.TcpClient$1.run()
java.lang.Thread.run()

run 函数 也是 所有java线程统一的入口点

但在抓包过程中，我们需要追溯到底是哪一段代码创建了这个线程实例. 而不仅仅是知道有这一个创建线程的函数被执行了。

所以我们需要去了解一个Java线程是怎么创建的，启动的。再去hook这个线程创建的函数，然后打印他的调用堆栈。