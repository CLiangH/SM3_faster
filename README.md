项目目标
=

加速SM3（软件）

项目技术
=

我们在此使用了减少计算量、循环展开、多线程等技术进行加速

代码说明
=

在扩展函数计算W以及W`时，我们使用循环展开，分别将3个循环以8，4，4的步长进行计算。

![image](https://github.com/CLiangH/Picture/blob/main/faster1.png)

同样，在CF函数中，我们将循环以4个步长进行，同时我发现每次执行循环时，代码都要算几次2**32，因此我们可以将其提到函数一开始，这样避免了计算重复数值，节约了时间。

![image](https://github.com/CLiangH/Picture/blob/main/faster2.png)

由于此项目是进行了10000次SM3的计算，因此我们可以使用多线程技术减少总运行时间，在此代码中，我使用了4个线程。

最终增速效果显著。


运行指导
=

本代码可直接运行


运行截图
=

![image](https://github.com/CLiangH/Picture/blob/main/faster3.png)
