# TODO

## 添加中断方式的支持

该模式目前未添加是因为下述情况还为解决：

我在轮询访问 GT1151 时发现，每次触摸抬起后 GT1151 的 0X814E 状态寄存器仍会产生三个 0x80 ，如果没有靠轮询去清除状态寄存器，GT1151 不会工作了。如果是中断方式使用 GT1151，这会出现永远无法读到触摸点的信息了。

如下图：

![](images/image-20201229155620035.png)