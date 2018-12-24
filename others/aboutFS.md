# 关于FS 

>  **[info] FS的含义 **  
>
>  functional specification（功能说明），是一个Excel形式的文件。 



以“应收款按数据”的FS为例，有三个sheet页，第一个是“处理逻辑”，这里定义了该模块功能的处理逻辑，Java开发时一般只需要看Java部分不需要看ABAP部分:

![pic1](../images/fs-pic1.png)



第二个sheet页是“表单结构”，定义了该模块需要用到的表及其中的字段信息:

![pic2](../images/fs-pic2.png)



第三个sheet页是“系统界面设计”，Java开发时先据此完成静态页面的开发：

![pic3](../images/fs-pic3.png)



以上就是对FS的简单介绍，开发过程中一般先全部看一遍，了解基本需求，然后根据“界面设计”绘制出静态页面，添加js行为，自己fake数据测试效果等，然后等ABAP接口开发完成，再去调用ABAP的接口。
