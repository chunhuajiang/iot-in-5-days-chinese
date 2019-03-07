# 3.4 在真实硬件上运行 Contiki

在本书中，我们使用的硬件开发平台是 Zolertia Z1 和 RE-Mote。当然也可以使用其它平台，但是不在本书的范围之内。

Contiki 的驱动和库通常是平台独立的。通过相关平台设置，大多数例程可以运行在 Z1 和 RE-Mote 之上。

Z1 平台的平台相关文件位于`examples/zolertia/z1`，RE-Mote 平台的平台相关文件位于`examples/zolertia/zoul`。此外，CC2538 相关的平台文件位于`examples/cc2538-common`，该文件夹下包含有 CC2538 RAM Cortex-M3相关例程和应用。

更多的关于平台和更新指导请看：

* [Zolertia website](http://www.zolertia)
* [Zolertia RE-Mote wiki pag](http://www.zolertia)e
* [Zolertia Z1 wiki page](https://github.com/Zolertia/Resources/wiki#the-z1-mote)

