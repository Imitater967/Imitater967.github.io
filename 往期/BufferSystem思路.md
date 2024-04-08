UI方面可以用unirx的mvp整
数据方面无非就是
buffereffect
- buffertype type
- uint level
- float duration
- bool persits
比如说减速buff，就应该又由速度处理系统函数检索所有的buff进行计算

比如。
1. 处理基础移动速度
2. 根据buff的优先级处理pre百分比移速和post百分百移速

buff系统不对其他系统进行操作，其他系统比如移动速度系统根据buff的数据来计算移动速度

最好单独弄一个asmdef

buff系统的拓展也单独一个asmdef